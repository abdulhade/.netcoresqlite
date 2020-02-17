
# API, .netcore 3, asp .net core, sqlite entity framework, multi projects and multi clients app(react and angular)

- The idea to create a web application to be able the IT manager cans includes your projects for your developers; and them developers can be able to read what projects you have, what status for, what application was developed in that project, what skills you used for and how much time you stayed in that project. 

## Creating classlib project to classes and generics functions
1. Create classlib project - >_ dotnet new classlib;
2. add the classes Company, Project, Manager;

## Creating a Database in SQLite(after you already installed that)
1.  CREATE TABLE "Company" ( "Id" INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE, "Name" TEXT NOT NULL UNIQUE );
2. CREATE TABLE "Manager" ( "Id" INTEGER NOT NULL UNIQUE, "Email" TEXT NOT NULL UNIQUE, "Passord" INTEGER NOT NULL );
3. CREATE TABLE "Project" ( "Id" INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE, "Name" TEXT NOT NULL UNIQUE );

## Creating the project to access the database

1. create a project dotnet core(webapi) infra to database access e basics actions
   - create sln file;
   - reference de project classlib;
   - delete the unnecessary files;
   - change de sdk, removing .web;
2. install entity framework package sqlite Microsoft.EntityFrameworkCore.Sqlite
3. install package AutoMapper.Extensions.Microsoft.DependencyInjection
4. create a database.cs file
   - create the class databasecontext inherit dbcontext;
   - create the classes represents de tables;
   - set them for dbset;
   - create the constructors of class to open database sqlite;
   - run dotnet ef database update;
5. Create de the classes that will makes de action crud in database;

## Creating the project for REST API

1. create a asp. net core without auth and  without https dotnet new webapi --auth None --no-https
2. install entity framework package sqlite Microsoft.EntityFrameworkCore.Sqlite
3. install package AutoMapper.Extensions.Microsoft.DependencyInjection
4. Configure AutoMapper no Startup.cs;
5. reference the projects classlib and infra;
6. create the controllers company, project and manager;
   - in the controllers call the infra classes;
7. install Swagger;
8. npm install -g @angular/cli - add a clientapp
9. 
