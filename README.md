# What am I thinking about at the moment?

On this page, I will post the topics I deal with and work on them as a developer and administrator of office automation.




<h2 align="center">September 2021</h2>
<!-----------------------------------------------------------------------------September----------------------------------------------------------------------------->

### 1- An experience about Office 365 administration:

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

### 2- Show loading before submiting form in a view (ASP .Net Core)

After the user clicked the submit button, I was going to load a JavaScript on the screen.
Everything worked fine if the user entered all the fields correctly.
But if Volidation found an error in the input information, the form would not be submitted and loading would still be displayed.
I did a lot of Google to be able to find out if the page is valid or not in jQuery or JavaScript, and show the loading if it is valid, otherwise the loading will not be displayed.
The file `jquery.validate.unobtrusive.js` runs after the functions written on the page so it always shows the form as valid. So I decided to add a line to the `jquery.validate.unobtrusive.js` file.


<h2 align="center">August 2021</h2>
<!-----------------------------------------------------------------------------August----------------------------------------------------------------------------->

### 1- Work on the graduation project of HackyourFuture.net

### 2- Deploy MERN web application to Heroku
- Increase heap memory from Heroku hosting for JavaScript 

### 3- Change user subscription in office 365 administration
- point: When you buy new subscription in Office 365 administrator panel and asign it to a user just wait 30 minuts to activate user outlook and all the things, instead do a lot and even call Microsoft support like me 😅.

### 4- ASP .NET Core Unit Of Work Repository Pattern:
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
var getJSON = function(url, callback) {
    var xhr = new XMLHttpRequest();
    xhr.open('GET', url, true);
    xhr.responseType = 'json';
    xhr.onload = function() {
      var status = xhr.status;
      if (status === 200) {
        callback(null, xhr.response);
      } else {
        callback(status, xhr.response);
      }
    };
    xhr.send();
};


getJSON('your API link',
function(err, data) {
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

firstFunc().then((data) => { // data will be set by myJson
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

- https://github.com/onodera-sf/AspNetCoreLocalizationDataAnnotation
- https://docs.microsoft.com/en-us/graph/tutorials/aspnet-core
- https://github.com/cnahmetcn/corecrud

### 2- Add event in Outlook calander from ASP.NET app

### 3- Create ASP.NET Core API and React.js

There is a very good tutorial here:

- https://www.youtube.com/watch?v=i8LymADs_U4
- https://www.youtube.com/watch?v=z5NsNtrl4Og
- https://github.com/CodAffection/React-js-Master-Detail-CRUD-with-Asp.Net-Web-API

### 4- Create GitHub API React.js
 - [Demo](https://github-react-project.herokuapp.com)
 - [Source](https://github.com/mahmood-ghaem/GitHub-React)

### 5- ASP.NET Core Logger

Get log from all activity of each user and save in database with IP address

### 6- UBL(Universal Business Language) in ASP.NET Core
- https://github.com/UblSharp/UblSharp
- https://en.wikipedia.org/wiki/Universal_Business_Language

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


