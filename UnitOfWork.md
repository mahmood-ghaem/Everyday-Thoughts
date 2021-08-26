## ASP .NET Core Unit Of Work Repository Pattern:

I use this pattern in all .NET projects, it is very efficient and optimal. Using the codes below, you can create the following files and implement your project with this pattern. I gave an example for an entity(BlogCategory) and you can create other entities in the same way.

Good Luck 👍


- Models/BlogCategory.cs
```c#
namespace Blog.Models
{
    public partial class BlogCategory
    {
        public BlogCategory()
        {

        }

        [Key]
        public int Id { get; set; }

        [Required(ErrorMessage = "Please enter {0}")]
        [StringLength(30)]
        [Display(Name ="Blog Category Caption")]
        public string Caption { get; set; }

        [AllowNull]
        [StringLength(400)]
        [Display(Name = "Blog Category Description")]
        public string Description { get; set; }

        [AllowNull]
        [Display(Name = "Activity Status")]
        public bool? Activity { get; set; }
    }
}
```
- DataAccess/IRepository/IBlogCategoryRepository.cs
```c#
namespace Blog.DataAccess.IRepository
{

    public interface IBlogCategoryRepository : IRepository<BlogCategory>
    {
        IEnumerable<SelectListItem> GetBlogCategoryListForDropDown();

        void Update(BlogCategory blogCategory);

        void UpdateActivity(int id, bool? status);
    }
}
```
- DataAccess/IRepository/IRepository.cs
```c#
namespace Blog.DataAccess.IRepository
{
    public interface IRepository<T> where T : class
    {
        T Get(int id);
        IEnumerable<T> GetAll(
            Expression<Func<T, bool>> filter = null,
            Func<IQueryable<T>, IOrderedQueryable<T>> orderby = null,
            string includeProperties = null
            );
        T GetFirstOrDefault(
            Expression<Func<T, bool>> filter = null,
            string includeProperties = null
            );
        void Add(T entity);
        ResultModel Remove(int id);
        ResultModel Remove(T entity);
    }
}
```
- DataAccess/IRepository/IUnitOfWork.cs
```c#
namespace Blog.DataAccess.IRepository
{
    public interface IUnitOfWork: IDisposable
    {
        IBlogCategoryRepository BlogCategory { get; }

        void Save();
    }
}
```
- DataAccess/Repository/BlogCategoryRepository.cs
```c#
namespace Blog.DataAccess.Repository
{
    public class BlogCategoryRepository : Repository<BlogCategory>, IBlogCategoryRepository
    {
        private readonly ApplicationDbContext _context;
        public BlogCategoryRepository(ApplicationDbContext context) : base(context)
        {
            _context = context;
        }

        public IEnumerable<SelectListItem> GetBlogCategoryListForDropDown()
        {
            return _context.BlogCategory.Select(i => new SelectListItem()
            {
                Text = i.Caption,
                Value = i.Id.ToString()
            });
        }

        public void Update(BlogCategory blogCategory)
        {
            var objFromDB = _context.BlogCategory.FirstOrDefault(s => s.Id == blogCategory.Id);
            objFromDB.Caption = blogCategory.Caption;
            objFromDB.Description = blogCategory.Description;

            _context.SaveChanges();
        }

        public void UpdateActivity(int id, bool? status)
        {
            var blogCategoryFromDB = _context.BlogCategory.FirstOrDefault(b => b.Id == id);
            blogCategoryFromDB.Activity = status;

            _context.SaveChanges();
        }
    }
}
```
- DataAccess/Repository/Repository.cs
```c#
namespace Blog.DataAccess.Repository
{
    public class Repository<T> : IRepository<T> where T : class
    {
        protected readonly DbContext Context;
        internal DbSet<T> dbset;

        public Repository(DbContext context)
        {
            Context = context;
            this.dbset = context.Set<T>();
        }

        public void Add(T entity)
        {
            dbset.Add(entity);
        }

        public T Get(int id)
        {
            return dbset.Find(id);
        }

        public IEnumerable<T> GetAll(Expression<Func<T, bool>> filter = null, 
                                     Func<IQueryable<T>, 
                                     IOrderedQueryable<T>> orderby = null, 
                                     string includeProperties = null)
        {
            IQueryable<T> query = dbset;
            if (filter != null)
            {
                query = query.Where(filter);
            }
            //includeProperties will be coma seperated
            if (includeProperties != null)
            {
                foreach (var includeProperty in includeProperties.Split(new char[] { ',' }, StringSplitOptions.RemoveEmptyEntries))
                {
                    query = query.Include(includeProperty);
                }
            }
            if (orderby != null)
            {
                return orderby(query).ToList();
            }
            return query.ToList();
        }

        public T GetFirstOrDefault(Expression<Func<T, bool>> filter = null, 
                                   string includeProperties = null)
        {
            IQueryable<T> query = dbset;
            if (filter != null)
            {
                query = query.Where(filter);
            }
            //includeProperties will be coma seperated
            if (includeProperties != null)
            {
                foreach (var includeProperty in includeProperties.Split(new char[] { ',' }, StringSplitOptions.RemoveEmptyEntries))
                {
                    query = query.Include(includeProperty);
                }
            }
            return query.FirstOrDefault();
        }

        public ResultModel Remove(int id)
        {

            try
            {
                T entityToRemove = dbset.Find(id);
                if (entityToRemove == null)
                {
                    return new ResultModel(Status.NotFound, false, Description.Not_Found, null);
                }
                return Remove(entityToRemove);



            }
            catch (Exception e)
            {
                return new ResultModel(Status.Failed, false, e.Message, null);
            }

        }

        public ResultModel Remove(T entity)
        {
            try
            {
                dbset.Remove(entity);
                return new ResultModel(Status.OK, true, Description.OK, null);
            }
            catch (Exception e)
            {
                return new ResultModel(Status.Failed, false, e.Message, null);
            }
        }
    }
}
```
- DataAccess/Repository/UnitOfWork.cs
```c#
namespace Blog.DataAccess.Repository
{
    public class UnitOfWork : IUnitOfWork
    {
        private readonly ApplicationDbContext _db;
        public UnitOfWork(ApplicationDbContext db)
        {
            _db = db;

            BlogCategory = new BlogCategoryRepository(_db);
        }

        public IBlogCategoryRepository BlogCategory { get; private set; }

        public void Dispose()
        {
            _db.Dispose();
        }

        public void Save()
        {
            _db.SaveChanges();
        }
    }
}
```
- DataAccess/ApplicationDbContext.cs
```c#
namespace Blog.DataAccess
{
    public class ApplicationDbContext : IdentityDbContext<ApplicationUser, ApplicationRole, string>
    {
        public ApplicationDbContext()
        {

        }
        public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options)
            : base(options)
        {
        }

        public DbSet<BlogCategory> BlogCategory { get; set; }
    }
}
```
- DataAccess/ResultModel.cs
```c#
namespace Blog.DataAccess
{
    public class ResultModel
    {
        public ResultModel()
        {
            this.StatusCode = Status.NotDefine;
            this.IsSucceed = null;
            this.Message = Description.NotDefine;
            this.ReturnData = null;
        }
        public ResultModel(Status StatusCode, bool? IsSucceed, string Message, string ReturnData)
        {
            this.StatusCode = StatusCode;
            this.IsSucceed = IsSucceed;
            this.Message = Message;
            this.ReturnData = ReturnData;
        }
        public Status StatusCode { get; set; }
        public bool? IsSucceed { get; set; }
        public string Message { get; set; }
        public string ReturnData { get; set; }
    }
    public class ResultTitle
    {
        public const string OK = "OK";
        public const string Failed = "Failed";
        public const string ModelIsNotValid = "ModelIsNotValid";
        public static string WrongCode = "WrongCode";
    }
    public enum Status
    {
        NotDefine=0,
        OK = 1,
        Failed = 2,
        NotFound = 3,
        ModelIsNotValid = 4,
        CredentialError = 5,
        FormNotCompleted=6
    }
    public static class Description
    {
        public static string NotDefine = "Not Define";
        public static string OK = "Job is completed.";
        public static string Failed = "There was an error.";
    }
}
```
- Models/ApplicationUser.cs
```c#
namespace Blog.Models
{
    public class ApplicationUser : IdentityUser
    {
        public ApplicationUser()
        {
        }

        [AllowNull]
        public string FirstName { get; set; }

        [AllowNull]
        public string LastName { get; set; }
    }
}
```
- Models/ApplicationRole.cs
```c#
namespace Blog.Models
{
    public class ApplicationRole : IdentityRole
    {
        public string Description { get; set; }
        public virtual ICollection<ApplicationRoleClaim> Claims { get; set; }
    }
}
```
- Models/ApplicationRoleClaim.cs
```c#
namespace Blog.Models
{
    public class ApplicationRoleClaim : IdentityRoleClaim<string>
    {
        public virtual ApplicationRole Role { get; set; }
    }
}
```
- Controllers/BlogCategoryController.cs
```c#
namespace Blog.Controllers
{
    public class BlogCategoryController : Controller
    {
        private readonly IUnitOfWork _unitOfWork;
        public BlogCategoryController(IUnitOfWork unitOfWork)
        {
            _unitOfWork = unitOfWork;
        }

        public IActionResult Index()
        {
            return View();
        }

        [HttpGet]
        public IActionResult GetAllRecords()
        {
            return Json(new { data = _unitOfWork.BlogCategory.GetAll(w => w.Activity != null) });
        }

        [HttpPost]
        [ValidateAntiForgeryToken]
        public IActionResult Delete(int id)
        {
            _unitOfWork.BlogCategory.Remove(id);
            _unitOfWork.Save();
            return Json(new { success = true, message = "Delete successful." });
        }

        [HttpPost]
        [ValidateAntiForgeryToken]
        public IActionResult ChangeActivity(int id, bool? status)
        {
            _unitOfWork.BlogCategory.UpdateActivity(id, status);
            if (status != null)
            {
                return Json(new { success = true, message = "Activity of record " + id + " changed to : " + status + "." });
            }
            else
            {
                return Json(new { success = true, message = "Record " + id + " deleted." });
            }
        }

        [HttpPost]
        [ValidateAntiForgeryToken]
        public IActionResult Upsert(string caption, string description, int? id)
        {
            BlogCategory blogCategory = new BlogCategory
            {
                Activity = false,
                Caption = caption,
                Description = description,
                Id = id ?? 0
            };
            if (ModelState.IsValid)
            {
                if (blogCategory.Id == 0)
                {
                    _unitOfWork.BlogCategory.Add(blogCategory);
                    _unitOfWork.Save();
                    return Json(new { success = true, message = "Insert succeed", status = "insert" });
                }
                else
                {
                    _unitOfWork.BlogCategory.Update(blogCategory);
                    _unitOfWork.Save();
                    return Json(new { success = true, message = "Update succeed", status = "update" });
                }
            }
            else
            {
                return Json(new { success = false, message = "Form is not valid, Please enter data correctly.", status = "nothing" });
            }
        }

    }
}
```
