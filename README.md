# dotnet-Core-cqrs-mediator-api ||Code Source Section
A .NET Core Web API with CQRS-Mediator design pattern implementation with Ef Core. It can run with Visual studio 2022 IDE with sql server database.

Give a Star! ⭐
----------------------------------------------------------------------------------------------------------------------
If you like this project, learn something or you are using it in your applications, please give  a star. Thanks!

Description
----------------------------------------------------------------------------------------------------------------------
Code repo with .NET Core Web API application implemented with CQRS, Mediator Pattern approach with Domain Driven Design.</br>
It has 3 branches as below</br>
1)**master(default)** => .NET Core Web API with CQRS-Mediator design pattern implementation with Ef Core. Code can run with Visual studio 2022 IDE with sql server database support. **Code repo present.**</br>
2)main => News announcement section, **No Code repo present** </br>
3)tutul/docker-support => Details of  docker support  on .NET Core Web API with CQRS-Mediator design pattern (master branch code repo). **Code repo present.**.</br>

# Code setup Instructions for *master* branch  at Local dev system 
----------------------------------------------------------------------------------------------------------------------
1)First ,Make sure to install Visual Studio 2022 IDE and .NET6 Frmwrk version on the Local system. </br>
2)Clone this code repo to the local system by using  a CMD like git clone <git repo url> . </br>
3)After cloning the code repo ,Open .sln file with Visual studio 2022 IDE and make the  WebApi project as startup project  .Please  update the sql database connection string at "WebApi/appsetting.json" file 
 as below  (key value) and try to rebuild at  top of the solution.  </br>
 
 >>"DatabaseConnection": "{give urs db connection string}" </br>
 
4)No build errors should come with Visual studio 2022 IDE and open package manager console  for database  migration purposes. </br>
5)At the package manager console try to run the below command by selecting "SampleProject.Core.SqlSever" project.
>>Add-Migration InitialCreate </br>
>>Update-Database </br>

6)Database migration should succeed and then  Build again the WebApi project.No build errors should come </br>
7)If migration process  and sql database connection string  is proper then have a run without debger mode in Visual studio 2022 IDE . App is loading at browser with swagger page with api end points as below</br>
![image](https://github.com/tutul2010/dotnet6-cqrs-mediator-api/assets/13733464/df42d4c9-3f7d-41e5-a452-17e51124fb3d)

Thanks @mghoreishi for your starting points.
