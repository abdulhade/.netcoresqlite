
# API, .netcore 3, asp .net core, sqlite entity framework, multi projects and multi clients app(react and angular)

- The idea to create a web application to be able the IT manager cans includes your projects for your developers; and them developers can be able to read what projects you have, what status for, what application was developed in that project, what skills you used for and how much time you stayed in that project.

## Creating a Database in SQLite(after you already installed and created the Database)

1. CREATE TABLE "Company" ( "Id" INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE, "Name" TEXT NOT NULL UNIQUE );
2. CREATE TABLE "Manager" ( "Id" INTEGER NOT NULL UNIQUE, "Email" TEXT NOT NULL UNIQUE, "Passord" INTEGER NOT NULL );
3. CREATE TABLE "Project" ( "Id" INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE, "Name" TEXT NOT NULL UNIQUE );

## Creating classlib project to classes and generics functions

1. Create classlib project - >_ dotnet new classlib;
2. add the classes Company, Project, Manager;

## Creating the project to access the database

1. Create classlib project - >_ dotnet new classlib;
2. create sln file - >_ dotnet new sln;
3. reference de project classlib above;
4. install entity framework package sqlite >_ dotnet add package Microsoft.EntityFrameworkCore.Sqlite ;
5. install package AutoMapper >_ dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection ;
6. run >_ dotnet ef database update , after coding according this project;
7. Create the classes that will makes de action crud in database;

## Creating the project for REST API

1. create a asp. net core without auth and without https >_ dotnet new webapi --auth None --no-https
2. install entity framework package sqlite >_ dotnet add package Microsoft.EntityFrameworkCore.Sqlite ;
3. install package AutoMapper >_ dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection ;
4. Configure AutoMapper no Startup.cs according with this project;
5. reference the projects classlib and the project access the database;
6. create the controllers company, project and manager;
   - in the controllers call the classes to return your result;
7. install Swagger and configure Startup.cs according with this project >_ dotnet add package Swashbuckle.AspNetCore;
