
# API, .netcore 3, asp .net core, sqlite entity framework, multi projects and multi clients app(react and angular);
## the idea to create a web application to be able the IT manager cans includes your projects for your developers; and them developers can be able to read what projects you have, what status for, what application was developed in that project, what skills you used for and how much time you stayed in that project. 

- Creating classlib project to classes and generics functions
1. Create classlib project - >_ dotnet new classlib;
2. add the classes Company, Project, Manager;

 - Creating the project to access the database
1. create a project dotnet core(webapi) infra to database access e basics actions;
1.1 create sln file;
1.2. reference de project classlib;
1.3. delete the unnecessary files;
1.4 change de sdk, removing .web;
2. install entity framework package sqlite Microsoft.EntityFrameworkCore.Sqlite
3. install package AutoMapper.Extensions.Microsoft.DependencyInjection
4. create a database.cs file 
4.1 create the class databasecontext inherit dbcontext;
4.2 create the classes represents de tables;
4.3 set them for dbset;
4.4 create the constructors of class to open database sqlite;
4.5 run dotnet ef database update
5. Create de the classes that will makes de action crud in database;

- project api -
1. create a asp. net core without auth and  without https dotnet new webapi --auth None --no-https
2. install entity framework package sqlite Microsoft.EntityFrameworkCore.Sqlite
3. install package AutoMapper.Extensions.Microsoft.DependencyInjection
4. Configure AutoMapper no Startup.cs;
5. reference the projects classlib and infra;
6. create the controllers company, project and manager;
6.1 in the controllers call the infra classes;
7. install Swagger;
8. npm install -g @angular/cli - add a clientapp
9. 

- create tables in the database
- create a UI project with two folders -

