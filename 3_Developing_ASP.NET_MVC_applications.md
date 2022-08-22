[Back to Syllabus](/README.md#course-syllabus)

## Learning Objectives
- Deploy ASP.NET MVC applications to Compute Engine
<br>

## Developing ASP.NET MVC Applications
- ASP.NET gives web application developers access to the dotnet framework
    - You can build applications on ASP.NET in the Google Cloud
    - In this module, we'll show you how. In this module, we'll look at how to create a web application using Microsoft's ASP.NET MVC framework or Google Cloud Platform Compute Engine
    - In Module 2 of this class, we looked at how to provision our Microsoft Windows Server and Microsoft SQL Server Infrastructure
    - We've got an Active Directory domain controller, a web server running Microsoft Internet Information Services, and a pair of Microsoft SQL Server instances running in an always on availability group

- Now it's time to build an application
    - We'll be coding a simple ASP.NET MVC application using C-Sharp
    - If you're a developer working with Microsoft technologies
    - We'll use Microsoft Visual Studio as our integrated development environment
    - We'll publish our application to Internet Information Services using Google Cloud tools for Visual Studio. If you're not a developer, just be aware that a web application delivers application functionality using the standard web browser. The browser accesses the application as a URL, and the server responds with dynamic outputs generated from data
    - In our case, from data stored in Microsoft SQL Server. ASP.NET MVC makes use of a widely used application architecture called Model View Controller. This architecture is frequently used when writing web applications. It allows for a clean separation of concerns between modeling, manipulating, and displaying data.
    - In our example, imagine that our application was running on a server located at http://mycorp.com. The contacts controller and details action method would be used to handle a request from a browser using that base URL, followed by slash contacts, the name of the controller, then slash details, the name of the action method. This would then be followed by a number that corresponds to the ID of one of our contact objects or one of our contact records in the database table. In the body of the details method in our control, we've written code using Microsoft Entity Framework to get the right code from SQL Server and return it to the contact object. The controller passes this object to the corresponding view, which formats it and returns it to the user's browser
    - As a developer, all you have to do is inherit from the DB context base class and add a property using the generic DbSet collection of your model class. Entity Framework will automatically create a database with a compatible scheme of your model class, if it doesn't already exist. Then show that your model objects can be created, retrieved, updated, and deleted in that database. I already mentioned that Visual Studio offers a great developer experience for coding ASP.NET MVC applications. Simply use the web project template and select the MVC option. You'll be able to automatically integrate your users existing Windows logins to get a seamless login experience against your new enterprise web application. One nice thing about writing ASP.NET MVC applications with Visual Studio is that the development environment will scaffold nearly all of the MVC code for us. All we have to do is to code the model and supply a class that knows how to map this model to the database with Entity Framework
    - Once you finish writing your code, then you'll also find it's straightforward to publish your application to Internet Information Services using Visual Studio, integrated Web Deploy
    - Google have made it even easier to deploy to Compute Engine virtual machines for Visual Studio using Google Cloud tools
<br>

## Hands-on Lab: Create an ASP.NET MVC Web Application
- Launch the Qwiklabs tool for open the Demo
    - Confirm the lab environment has been setup correctly
    - Install Microsoft Visual Studio 2015 Community Edition
    - Create an ASP.NET MVC application
    - Integrate Data Access with Entity Framework
    - Re-publish the ASP.NET application
<br>

[Go to Next Module](./4_Configuring_Resilient_Workloads.md)
