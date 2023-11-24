#See https://aka.ms/customizecontainer to learn how to customize your debug container and how Visual Studio uses this Dockerfile to build your images for faster debugging.

### PREPARE
FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base
WORKDIR /app

### Copy csproj and sln and restore as distinct layers

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
ARG BUILD_CONFIGURATION=Release
WORKDIR /src
COPY ["src/04. Endpoints/WebApi/WebApi.csproj", "src/04. Endpoints/WebApi/"]
COPY ["SampleProject.Core.SqlServer/SampleProject.Core.SqlServer.csproj", "SampleProject.Core.SqlServer/"]
COPY ["src/01.Core/SampleProject.Core.Domain/SampleProject.Core.Domain.csproj", "src/01.Core/SampleProject.Core.Domain/"]
COPY ["src/01.Core/SampleProject.Core.ApplicationService/SampleProject.Core.ApplicationService.csproj", "src/01.Core/SampleProject.Core.ApplicationService/"]
RUN dotnet restore "./src/04. Endpoints/WebApi/./WebApi.csproj"
COPY . .
WORKDIR "/src/src/04. Endpoints/WebApi"
RUN dotnet build "./WebApi.csproj" -c $BUILD_CONFIGURATION -o /app/build

### PUBLISH

FROM build AS publish
ARG BUILD_CONFIGURATION=Release
RUN dotnet publish "./WebApi.csproj" -c $BUILD_CONFIGURATION -o /app/publish /p:UseAppHost=false

### RUNTIME IMAGE
FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENV ASPNETCORE_URLS=http://+:80
EXPOSE 80
ENTRYPOINT ["dotnet", "WebApi.dll"]