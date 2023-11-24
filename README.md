# dotnet-Core-cqrs-mediator-api - docker support in windows 10 enviroment
A .NET Core Web API CQRS-Mediator design patterns implementation with Ef Core,on top of  Clean Architecture at .NET6.

Give a Star! ⭐
----------------------------------------------------------------------------------------------------------------------
If you like this project, learn something or you are using it in your applications, please give it a star. Thanks!

Description
----------------------------------------------------------------------------------------------------------------------
Code repo with .NET Core Web API application implemented with CQRS, Mediator Pattern approach and Clean Architecture. </br>
It require </br>
1)windows 10/11 with hyperbios enable. </br>
2)docker desktop installed. </br>
3)Visual Studio 2022 IDE and .NET6 version installed. </br>
4)stable internet connectivity. </br>

# Code setup Instructions of  *tutul/docker-support* branch on dev system 
----------------------------------------------------------------------------------------------------------------------
1)First ,Make sure to install Visual Studio 2022 IDE and .NET6 version on the Local system. </br>
2)Clone this code repo to the local system by using  a CMD like git clone <git repo url> .</br>
3)After cloning the code repo ,Open .sln file with Visual studio 2022 IDE and make the  WebApi project as startup project .Please  update the sql database connection string at "WebApi/appsetting.json" file 
and try to rebuild on top of the solution. </br>
4)No build errors should come with Visual studio 2022 IDE and open package manager console  for database  migration purposes. </br> 
5)At the package manager console try to run the below command by selecting "SampleProject.Core.SqlSever" project.
>>Add-Migration InitialCreate </br>
>>Update-Database </br>

6)Database migration should be succeed and then  run the WebApi project with debug mode with Visual studio 2022 IDE .It opens with  swagger page-api endpoints  at the browser. </br>
7)Open application root folder in powershell as below  and run 'docker compose up --build' command then it will start createing linux images and starting run at linux contaoner</br>

![image](https://github.com/tutul2010/dotnet6-cqrs-mediator-api/assets/13733464/f7efe750-b628-4d1e-8bf0-8eea27f9648c)

8)The linux container images exposes at  tcp # 8081 port and then  open a chorme browser and type at addressber  weburl as 'http://localhost:8081/ArticleCategory/GetArticleCategories' or 'http://localhost:8081/Article/GetArticles' . </br>

![image](https://github.com/tutul2010/dotnet6-cqrs-mediator-api/assets/13733464/e3e23fba-9410-447a-8491-b5f1c2561ba6)

WebApi endpoints loading at chorme browser as below
![image](https://github.com/tutul2010/dotnet6-cqrs-mediator-api/assets/13733464/4a82189d-98ef-40c7-bb52-99f9791bfff6)

Thanks @mghoreishi for your starting points.
