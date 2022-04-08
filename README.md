# What am I thinking about at the moment?

On this page, I will post the topics I deal with and work on them as a developer and administrator of office automation.

<h2 align="center">April 2022</h2>
<!-----------------------------------------------------------------------------April----------------------------------------------------------------------------->

### 1- Unit Test

- [.NET 5 REST API Unit Testing and TDD](https://www.youtube.com/watch?v=dsD0CMgPjUk)
- `Assert.Matches("[A-Z]{1}[a-z]+ [A-Z]{1}[a-z]+", result);`


<h2 align="center">March 2022</h2>
<!-----------------------------------------------------------------------------March----------------------------------------------------------------------------->

### ASP.NET-Microservices

<h2 align="center">February 2022</h2>
<!-----------------------------------------------------------------------------February----------------------------------------------------------------------------->

### 1- Docker

- #### Learn Linux commands useful in Docker [View Page](./LinuxCommands.md)
- #### Some useful Docker commands [View Page](./Docker-Commands.md)

### 2- Google PageSpeed Insights

 - [Get Started with the PageSpeed Insights API](https://developers.google.com/speed/docs/insights/v5/get-started)
 - [PageSpeed Insights](https://pagespeed.web.dev/)
 - [Extracting Google PageSpeed performance score in .NET](https://davecallan.com/getting-google-pagespeed-performance-score-dotnet/)

### 3- Debug ASP.NET Core apps with IIS
  - [Reference](https://docs.microsoft.com/en-us/visualstudio/debugger/how-to-enable-debugging-for-aspnet-applications?view=vs-2019#iis)
  - [Video](https://www.youtube.com/watch?v=NKehTIFvZCA)

### 4- Error 405 – Methods not Allowed in ASP.NET Core PUT and DELETE requests in published host server - IIS

Add to `web.config`:

```c#
<system.webServer>
  <modules runAllManagedModulesForAllRequests="false">
    <remove name="WebDAVModule" />
  </modules>
</system.webServer>
```

<h2 align="center">January 2022</h2>
<!-----------------------------------------------------------------------------January----------------------------------------------------------------------------->

### 1- Delete a Commit on Github Repository

- git reset --hard 3813803
- git push --force origin master

[Refrence](https://stackoverflow.com/questions/38402396/how-to-delete-commits-from-git-on-github-and-bitbucket)

### 2- Create and setup DevOps account

- Work with Backlogs
- Work with Sprints
- Repos & connect with Visual Studio 2019
- Pipelines
- Release code and db to Azure VM

### 3- Microsoft Azure

- Start free subscription
- Create Virtual Machine as IIS server
- Create Virtual Machine as SQL server
- Connect servers in one resource group
- Create SQL Database
- Create Web Application
- Publish with Visual Studio 2019 to Azure IIS VM or WebApp

### 4- IdentityServer 4

- [Oficial page](https://identityserver4.readthedocs.io/en/latest)
- [Usefull page](https://www.dntips.ir/post/2903/%D8%A7%D9%85%D9%86-%D8%B3%D8%A7%D8%B2%DB%8C-%D8%A8%D8%B1%D9%86%D8%A7%D9%85%D9%87%E2%80%8C%D9%87%D8%A7%DB%8C-asp-net-core-%D8%AA%D9%88%D8%B3%D8%B7-identityserver-4x-%D9%82%D8%B3%D9%85%D8%AA-%D8%A7%D9%88%D9%84-%D9%86%DB%8C%D8%A7%D8%B2-%D8%A8%D9%87-%D8%AA%D8%A7%D9%85%DB%8C%D9%86-%DA%A9%D9%86%D9%86%D8%AF%D9%87%E2%80%8C%DB%8C-%D9%87%D9%88%DB%8C%D8%AA-%D9%85%D8%B1%DA%A9%D8%B2%DB%8C)

1. ##### Udemy Course

   - [Secure .Net Microservices with IdentityServer4 OAuth2,OpenID](https://www.udemy.com/course/secure-net-microservices-with-identityserver4-oauth2openid)
   - [Source repo](https://github.com/aspnetrun/run-aspnet-identityserver4)

2. ##### IdentityServer4 .NET Core 3.1

   - [Quickstart](https://deblokt.com/2020/01/24/01-identityserver4-quickstart-net-core-3-1)
   - [EntityFramework](https://deblokt.com/2020/01/24/02-identityserver4-entityframework-net-core-3-1)
   - [ASP.NET Core Identity](https://deblokt.com/2020/01/24/04-part-1-identityserver4-asp-net-core-identity-net-core-3-1)

### 5- ASP.NET Identity And IdentityServer4

[Refrence](https://feras.blog/how-to-use-asp-net-identity-and-identityserver4-in-your-solution)

### 6- Research about Scrum

[Refrence](https://virgool.io/@sadeqnickbakht/%D8%A2%D9%85%D9%88%D8%B2%D8%B4-%D8%A7%D8%B3%DA%A9%D8%B1%D8%A7%D9%85-scrum-qqmstf2clhfg)

### 7- How to Boot Windows from SD Card

[Link](https://www.partitionwizard.com/clone-disk/boot-from-sd-card.html)

### 8- Permission-Based Authorization in ASP.NET Core 5

- [Reference](https://codewithmukesh.com/blog/permission-based-authorization-in-aspnet-core)
- [Reference](https://benfoster.io/blog/customize-authorization-response-aspnet-core)

### 9- Script to change table ownership in MS SQL - from admin_demo to dbo

```
EXEC sp_changeobjectowner '[admin_demo].[AspNetUsers]', dbo
```

### 10- GitHub Action to automaticaly deploy

### 11- ASP.NET Core seed data

[View Code](./SeedData.NetCore.md)

### 12- ASP.Net Core DTO and Auto Mapper

[View Code](./AutoMapperDTO.md)

<h2 align="center">December 2021</h2>
<!-----------------------------------------------------------------------------December----------------------------------------------------------------------------->

### 1- Outlook Calendar Integration with ASP .NET Core

[Refrence](https://www.youtube.com/watch?v=19WNyihLgR0&list=PLlaJNuOIC_9-xCapKiQ-T5TKVu8ZSLpQR&index=6)

[My Issue](https://stackoverflow.com/questions/70362288/asp-net-core-3-1-problem-get-access-token-with-microsoft-oauth-2-0)

### 2- Use the Microsoft Graph API

- Authentication and Authorization
- Get a token
- Use the access token to call Microsoft Graph
- Use the refresh token

### 3- Entity Framework Core zero-or-one to zero-or-one relation

[Refrence](https://entityframeworkcore.com/knowledge-base/54497784/entity-framework-core-zero-or-one-to-zero-or-one-relation)

[My Issue](https://stackoverflow.com/questions/70423589/entity-framework-core-one-to-zero-or-one-on-delete)

[Configure One-to-Zero-or-One Relationship in Entity Framework 6](https://www.entityframeworktutorial.net/code-first/configure-one-to-one-relationship-in-code-first.aspx)

### 4- Asp .Net Core 3.1 create a service to send email confirmation

[My Issue](https://stackoverflow.com/questions/70438306/asp-net-core-3-1-create-a-service-to-send-email-confirmation)

<h2 align="center">November 2021</h2>
<!-----------------------------------------------------------------------------November----------------------------------------------------------------------------->

### 1- ASP .Net Core UserIdentity

#### Subject

Get all users in a role with other navigation property related to each user.

#### Solution

```C#
//The first step: get all user id collection as userids based on role from (*1) _context.UserRoles
var userIds = _context.UserRoles.Where(w => w.RoleId == "ID of role").Select(b => b.UserId).Distinct().ToList();

//The second step : find all users collection from _context.Users  which 's Id is contained at userIds
// also use Include and ThenInclude to fill navigation properties
var users = _context.Users.Include(i => i.(*2)).ThenInclude(j => j.(*3)).Include(b => b.(*4))
                          .Where(w => userIds.Any(c => c == w.Id)).ToList();

// (*1) private readonly ApplicationDbContext _context;
// (*2), (*3), (*4) each navigation property you want to fill in.
```

[Refrence](https://forums.asp.net/t/2129247.aspx?Get+all+users+with+a+specific+role+in+ASP+NET+Core+2+0)

### 2- Send email by WPF

### 3- Select records count from multiple tables in a single query

```C#
 public IEnumerable<ApplicationUserActivitiesVM> GetUserActivities(string userId)
        {
            var result = from dummyRow in new List<string> { "X" }
                         join blog in _context.Blog on 1 equals 1 into bg
                         join ublog in _context.Blog.Where(w => w.AuthorId == userId) on 1 equals 1 into ubg
                         join interview in _context.CandidateInterview on 1 equals 1 into iw
                         join candidate in _context.UserRoles.Where(w => w.RoleId == "role id placed here") on 1 equals 1 into ce

                         select new ApplicationUserActivitiesVM()
                         {
                             BlogsCount = bg.Count(),
                             CandidatesCount = ce.Count(),
                             InterviewsCount = iw.Count(),
                             UserBlogs = ubg.Select(s=>new UserActivityBlog(s)).ToList(),
                         };

            return result;
        }
```

[Refrence](https://stackoverflow.com/questions/21182116/select-records-count-from-multiple-tables-in-a-single-query)

<h2 align="center">October 2021</h2>
<!-----------------------------------------------------------------------------October----------------------------------------------------------------------------->

### 1- Printer problem

[How to Clean Clogged Printhead Nozzles for Epson Printers](https://www.youtube.com/watch?v=ep77Wj_Vq6k)

[Clean sensor cartridge](https://www.youtube.com/watch?v=3HeBhiIQFUg&t=289s)

Be careful not to get the sensors of cartridge, wet when cleaning nozzeles.

### 2- Use google Chart in ASP .Net Core

[Link](https://developers.google.com/chart)

### 3- Blog

[Link](https://www.qadrit.nl/Public/Blog)

### 4- Customize UserIdentity of ASP .Net Core

### 5- Notification in ASP .Net Core

### 6- Entity Framework Core - Include Multiple Levels of a Property for a Collection

[Link](https://entityframeworkcore.com/knowledge-base/53001072/entity-framework-core---include-multiple-levels-of-a-property-for-a-collection)

```C#
var blogs = context.Blogs
    .Include(blog => blog.Posts)
        .ThenInclude(post => post.Author)
    .ToList();
```

<h2 align="center">September 2021</h2>
<!-----------------------------------------------------------------------------September----------------------------------------------------------------------------->

### 1- An experience about Office 365 administration

We have a web domain that we added in the Office admin panel.
We have created several users for this domain and all of them use their email to access Outlook.

I transferred the domain from the account of the company that bought it for us to our account.
I also changed the hosting. I replaced the site that was previously based on WordPress with a new version that I wrote based on ASP .NET Core: [de-medewerker.nl](https://de-medewerker.nl).

After these events, everything worked fine, except for users' emails, which did not have the ability to receive emails.
After researching, I realized that I had to change Name Servers in hosting.

<div align="center">
  <img src='/Data/Nameservers-Office365.png' alt='NameServers related to office 365' />
</div>

> Office 365 admin panel -> Settings -> Domains -> DNS records 👆

[Related article by Microsoft](https://docs.microsoft.com/en-US/microsoft-365/admin/get-help-with-domains/dns-basics?WT.mc_id=365AdminCSH_inproduct&view=o365-worldwide)

### 2- Show loading before submiting form in a view (ASP .Net Core)

After the user clicked the submit button, I was going to show a loading DIV by JavaScript on the screen and disable the all buttons. 💡

Everything worked fine if the user entered all the fields correctly.

But if Volidation found an error in the input information, the form would not be submitted and loading would still be displayed. 🤷

I did a lot of Google to be able to find out if the page is valid or not in jQuery or JavaScript, and show the loading if it is valid, otherwise the loading will not be displayed.

The file `jquery.validate.unobtrusive.js` runs after the functions written on the page so when I checked on the page with JavaScript whether the form is valid or not, the answer was always true. So I decided to add some lines to the `jquery.validate.unobtrusive.js` file.

```javascript
function onErrors(event, validator) {
  // 'this' is the form element
  var container = $(this).find('[data-valmsg-summary=true]'),
    list = container.find('ul');

  if (list && list.length && validator.errorList.length) {
    list.empty();
    container
      .addClass('validation-summary-errors')
      .removeClass('validation-summary-valid');

    $.each(validator.errorList, function () {
      $('<li />').html(this.message).appendTo(list);
    });
  }
  // This is my code added, and If an error occurs, it will hide the loading.
  if ($('#AjaxLoader').length) {
    $('#AjaxLoader').hide();
  }
}
```

I know this may not be the best way, but it solved my problem.😉

### 3- Working on Job Board CRM

[Link](https://de-medewerker.nl/Common/Home/ZoekWerk)

### 4- Transfer hosting and database of a WordPress web site

[Link](https://www.tigroep.nl)

### 5- Working with Gravity Form in WordPress

### 6- Following the problems I had with adding the domain in Office 365, in the last step, I realized that some users of Office 365 have problems sending and receiving to some email addresses and encounter problems

#### And solutions

After you add the domain to the Office 365 admin panel, you need to change the DNS in the domain hosting (base on Microsoft NS) and then disable the email service in the hosting to prevent conflict.

<div align="center">
  <img src='/Data/DisableMailServiceInHosting.png' alt='Disable Mail Service In Hosting' />
</div>

> Domain Dashboard -> Email -> Email Settings (in Plesk) 👆

In the domain registrar, you only need to define NS hosting, and in DNS hosting, you need to define DNS records.

<h2 align="center">August 2021</h2>
<!-----------------------------------------------------------------------------August----------------------------------------------------------------------------->

### 1- Work on the graduation project of HackyourFuture.net

### 2- Deploy MERN web application to Heroku

- Increase heap memory from Heroku hosting for JavaScript

### 3- Change user subscription in office 365 administration

- point: When you buy new subscription in Office 365 administrator panel and asign it to a user just wait 30 minuts to activate user outlook and all the things, instead do a lot and even call Microsoft support like me 😅.

### 4- ASP .NET Core Unit Of Work Repository Pattern

I use this pattern in all .NET projects, it is very efficient and optimal.
Using the code page, you can create the following files and implement your project with this pattern.
I gave an example for an entity(BlogCategory) and you can create other entities in the same way.

Good Luck 👍

[View code page](https://github.com/mahmood-ghaem/Everyday-Thoughts/blob/main/UnitOfWork.md)

- Models/BlogCategory.cs
- DataAccess/IRepository/IBlogCategoryRepository.cs
- DataAccess/IRepository/IRepository.cs
- DataAccess/IRepository/IUnitOfWork.cs
- DataAccess/Repository/BlogCategoryRepository.cs
- DataAccess/Repository/Repository.cs
- DataAccess/Repository/UnitOfWork.cs
- DataAccess/ApplicationDbContext.cs
- DataAccess/ResultModel.cs
- Models/ApplicationUser.cs
- Models/ApplicationRole.cs
- Models/ApplicationRoleClaim.cs
- Controllers/BlogCategoryController.cs

### 5- Working on QadrIT.nl web site

[Link](https://www.qadrit.nl)

<h2 align="center">July 2021</h2>
<!------------------------------------------------------------------------------July------------------------------------------------------------------------------>

### 1- Research about Microsoft Dynamic ATS (Applicant Tracking System)

- [How to manage open jobs in Dynamics 365](https://www.youtube.com/watch?v=K988bQ1WcRM)

### 2- WP ERP Pro

- [Installing WP ERP Pro on a WordPress web site](https://wperp.com/)
- [HR Frontend](https://wperp.com/14369/introducing-all-new-wordpress-hr-frontend/)
- [First using ERP Software](https://wperp.com/87054/how-to-use-erp-software-in-your-business/)
- [Payroll](https://wperp.com/docs/accounting-add-ons/payroll/)
- [Recruitment](https://wperp.com/docs/hrm-add-ons/recruitment/)

### 3- Work on WordPress Administration

- [Recover a WordPress web site (deactivate all plugins)](https://wordpress.org/support/article/faq-troubleshooting/)
- [Research about WordPress Database and Tables](https://wp-staging.com/docs/the-wordpress-database-structure/)

### 4- Email marketing with weMail WordPress plugin

- Instalation and configuration
- Administration
- Create Campaigns to send email to users
- Create template email

### 5- SharePoint

- Administration
- Create and manage web pages

### 6- Styling React.js with WebPack for HYF graduation project

### 7- ASP.NET Core fetch data from an API

- [Deserialize json to IEnumerable](https://stackoverflow.com/questions/51359062/deserialize-json-to-ienumerable-in-c-sharp-asp-net-core)
- [Getting data from WP-ERP API](https://wperp.com/docs/hrm-add-ons/recruitment/#global-api)

### 8- Custome theme for WordPress

- [Learning document in Persian language](https://hamyarwp.com/wordpress-theme-development/?__cf_chl_jschl_tk__=cb3061d41af81f2d0688aef7ea0ca6f1e8f9008f-1626256148-0-AfzmH54fzWDrq3exN16hVZwA6yqDzkrV0QBv9nkzhiZeX7KWksBT_e_ijAb4apvzkwCs8NquQDmSr3ItFY6mVdrZpwGvJ1rGt_kE1TB9GTLjhFOklN7GalUAg0bhzswxUaDii2Shs6z_gMrw4YmkZ__8Bw_mQGQSc16_Xu1IBZvGSfpTOuunktCdwRyCrOd5N6MpscMUfvNZCluls_EPchx6SNULoUffNjpNkfedI8xoNSZfjIZ2cAUZPMgY4eRd678V3Hxcxyoih8y34YXp5nueZdgztbw4pAYDyVAYxJ2pZpWkEqfRgnBxQGvU1qp4dY0OtPYQOoR1gGqUQGSBQFNfCUXlp653Yglkp_P6wbFAyAsvVn3-SPkfXwMb9DTkAm2DMsfnpa85GWH4tiNPAYxWBi1yAE7u2ZgISDXqTZow8ccBbMqZp0r9qYD_6AmdPKkjUh_MUEg9mJP72z3d4l41M6KTSUrbVKLdbC25p0FekHCWAypwXiJ_oMf7Zh0E0A)

### 9- Create search result page for HYF graduation project

### 10- Adyen checkout payment

- [Optimize your checkout](https://www.adyen.com/knowledge-hub/guides/payments-training-guide/optimize-your-checkout)
- [Adyen online payment integration demos](https://github.com/adyen-examples/adyen-node-online-payments)
- [Drop-in tutorial: Node.js + Express](https://www.youtube.com/watch?v=C2hdSa3QJIk)
- [Adyen Docs](https://docs.adyen.com/development-resources/api-credentials#generate-your-api-key)

### 11- WordPress Plugin

- [Basic example of wordpress plugin to CRUD](https://github.com/eduardoarandah/wordpress-crud-example)
- [Learn how to create WordPress Plug-in](https://darkoobweb.com/wordpress-plugin-learning/)

### 12- Pass props to another component onclick of a button in React.js

```javascript
import React from 'react';
import { useHistory } from 'react-router-dom';
function Component({ product }) {
  const history = useHistory();
  const handlerButton = () =>
    history.push({
      pathname: '/yourRoute',
      state: your object you want to send,
    });
  return (
    <div>
     <Button onClick={handlerButton}>Button Text</Button>
    </div>
  );
}
export default Component;
```

### 13- Transfer WordPress site to another hosting

- [Move your WordPress site to another domain](https://help.one.com/hc/en-us/articles/115005585969-Move-your-WordPress-site-to-another-domain#step-6)
- [Changing The WordPress URL](https://wordpress.org/support/article/changing-the-site-url/)

### 14- How to get JSON from API in JavaScript?

- [Reference](https://stackoverflow.com/questions/12460378/how-to-get-json-from-url-in-javascript)

```javascript
var getJSON = function (url, callback) {
  var xhr = new XMLHttpRequest();
  xhr.open('GET', url, true);
  xhr.responseType = 'json';
  xhr.onload = function () {
    var status = xhr.status;
    if (status === 200) {
      callback(null, xhr.response);
    } else {
      callback(status, xhr.response);
    }
  };
  xhr.send();
};

getJSON('your API link', function (err, data) {
  if (err !== null) {
    alert('Something went wrong: ' + err);
  } else {
    alert('Your query count: ' + data.query.count);
  }
});
```

Another way:

```javascript
const firstFunc = async () => {
  const response = await fetch(apiUrl);
  const myJson = await response.json(); //extract JSON from the http response
  return myJson;
};

firstFunc().then((data) => {
  // data will be set by myJson
  secondFunc(data);
});
```

### 15- OpenStreetMap

- [Creating A Map With Markers](https://mediarealm.com.au/articles/openstreetmap-openlayers-map-markers)
- [Nominatim Wiki](https://wiki.openstreetmap.org/wiki/Nominatim#API)
- [Nominatim Doc](http://nominatim.org/release-docs/latest/)

<h2 align="center">June 2021</h2>
<!------------------------------------------------------------------------------June------------------------------------------------------------------------------>

### 1- Create WordPress Plugin

- [How to Create Your First WordPress Plugin](https://www.dreamhost.com/blog/how-to-create-your-first-wordpress-plugin)

### 2- Access Asp .Net to WordPress Database

### 3- Relational lists in sharepoint

### 4- Create mobile app for sharepoint lists

### 5- Automate task in sharepoint, Add event to outlook calander related sharepoint list task

### 6- Change DNS recodrs for a domain to resolve it to another hosting

### 7- Calculate an area on Google Map in a web page

- [Like IKEA Page](https://sveasolar.com/nl/ikea)

### 8- Design web site for Bazaar

This is final HYF project.

- [Demo](https://mahmood-ghaem.github.io/Bazar-HYF-Project/index.html)
- [Source](https://github.com/mahmood-ghaem/Bazar-HYF-Project)

### 9- How to debug IIS hosted asp.net web application in visual studio?

There are a lot of contents in internet for this question but I went ahead with this article and it worked well, contrary to Microsoft's confusing tutorials 😉

- <a href="./Data/How to debug IIS hosted asp.net web application in visual studio.pdf" target="_blank">Article</a>

### 10- 5 hours debuging just for one mistake 🤦‍♂️

- My new web application doesn't have web.config so in deployment(upload to hosting) startup.cs couldn't access appsettings.Development.json file and my project couldn't send confirmation email after user registration.
- To create web.config automatically --> right click on project in sulotion explorer --> click properties --> in build tab just make some changes to web.config will be create (I don't know what exactly I did.)

### 11- Learn to work with [Figma](https://www.figma.com)

- I prefered Adobe XD

<h2 align="center">May 2021</h2>
<!------------------------------------------------------------------------------May------------------------------------------------------------------------------>

### 1- Globalization and Localization in ASP.NET Core

I'm trying to learn how to create a multilingual web application?

- <https://github.com/onodera-sf/AspNetCoreLocalizationDataAnnotation>
- <https://docs.microsoft.com/en-us/graph/tutorials/aspnet-core>
- <https://github.com/cnahmetcn/corecrud>

### 2- Add event in Outlook calander from ASP.NET app

### 3- Create ASP.NET Core API and React.js

There is a very good tutorial here:

- <https://www.youtube.com/watch?v=i8LymADs_U4>
- <https://www.youtube.com/watch?v=z5NsNtrl4Og>
- <https://github.com/CodAffection/React-js-Master-Detail-CRUD-with-Asp.Net-Web-API>

### 4- Create GitHub API React.js

- [Demo](https://github-react-project.herokuapp.com)
- [Source](https://github.com/mahmood-ghaem/GitHub-React)

### 5- ASP.NET Core Logger

Get log from all activity of each user and save in database with IP address

### 6- UBL(Universal Business Language) in ASP.NET Core

- <https://github.com/UblSharp/UblSharp>
- <https://en.wikipedia.org/wiki/Universal_Business_Language>

### 7- HYF Node.js Test

An exam about Node.js module

- [Repository](https://github.com/mahmood-ghaem/HYF-Node.js-Test)

### 8- Managing GitHub Company Page

<h2 align="center">April 2021</h2>
<!------------------------------------------------------------------------------April------------------------------------------------------------------------------>

### 1- JavaScript Quiz

A project created with JavaScript

- [Demo](https://mahmood-ghaem.github.io/browser-quiz/index.html)
- [Source](https://github.com/mahmood-ghaem/browser-quiz)

### 2- Predict Nationality

A project created with JavaScript

- [Demo](https://mahmood-ghaem.github.io/API-JavaScript-Project/index.html)
- [Source](https://github.com/mahmood-ghaem/API-JavaScript-Project)

### 3- Node.js-Express CrashCourse

- [Demo](https://splashy-candy-skirt.glitch.me)
- [Source](https://github.com/mahmood-ghaem/Node.js-Express-CrashCourse)
- [Reference](https://www.youtube.com/watch?v=L72fhGm1tfE)

### 4- Node.js Express API

- [Source](https://github.com/mahmood-ghaem/Node.js_Express_API)
- [Reference](https://www.youtube.com/watch?v=l8WPWK9mS5M)

### 5- Node.js Blog

- [Demo](https://hyf-blog.herokuapp.com)
- [Source](https://github.com/mahmood-ghaem/hyf-blog)
- [Reference](https://github.com/v1t03r/E_Commerce-MongoDB-Node.js)

<h2 align="center">March 2021</h2>
<!------------------------------------------------------------------------------March------------------------------------------------------------------------------>

### 1- HTML-CSS Tips & Tricks

- [Repository](https://github.com/mahmood-ghaem/HTML-CSS-TipsAndTricks)

<h2 align="center">February 2021</h2>
<!------------------------------------------------------------------------------February------------------------------------------------------------------------------>

### 1- JavaScrip CodePieces

I put everything I have learned about JavaScript in this repository.

- [Repository](https://github.com/mahmood-ghaem/JavaScrip-CodePieces)

### 2- using-apis-test-got

An exam about using API module

- [Repository](https://github.com/mahmood-ghaem/using-apis-test-got)

<h2 align="center">January 2021</h2>
<!------------------------------------------------------------------------------January------------------------------------------------------------------------------>

### 1- HTML-CSS Homework of HackYourFuture

- [All 3 weeks](https://mahmood-ghaem.github.io/HYF-Module-HTMLCSSGIT)
