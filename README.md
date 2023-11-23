# dotnet-Core-cqrs-mediator-api
A .NET Core Web API CQRS implementation with Ef Core,Mediator, Cqrs and DDD using Clean Architecture at .NET6.

Give a Star! ⭐
----------------------------------------------------------------------------------------------------------------------
If you like this project, learn something or you are using it in your applications, please give  a star. Thanks!

Description
----------------------------------------------------------------------------------------------------------------------
Code repo with .NET Core Web API application implemented with CQRS, Mediator Pattern approach with  Domain Driven Design.

# Code setup Instructions for *master* branch  at Local dev system 
----------------------------------------------------------------------------------------------------------------------
1)First ,Make sure to install Visual Studio 2022 IDE and .NET6 Frmwrk version on the Local system. </br>
2)Clone this code repo to the local system by using  a CMD like git clone <git repo url> .</br>
3)After cloning the code repo ,Open .sln file with Visual studio 2022 IDE and make the  WebApi project as startup project  .Please  update the sql database connection string at "WebApi/appsetting.json" file 
 as below  (key value) and try to rebuild at  top of the solution and run without debger mode. </br>
 
 >>"DatabaseConnection": "{give urs db connection string}" </br>
 
4)No build errors should come with Visual studio 2022 IDE and open package manager console  for database  migration purposes. </br>
5)At the package manager console try to run the below command by selecting "SampleProject.Core.SqlSever" project.
>>Add-Migration InitialCreate </br>
>>Update-Database </br>

6)Database migration should succeed and then  run the WebApi project with debug mode with Visual studio 2022 IDE .It opens with  swagger page-api endpoints  at the browser. </br>
7)If migration and sql database connection is proper then app is loading swagger page with api end points as below</br>
![image](https://github.com/tutul2010/dotnet6-cqrs-mediator-api/assets/13733464/df42d4c9-3f7d-41e5-a452-17e51124fb3d)

Thanks @mghoreishi for your starting points.
