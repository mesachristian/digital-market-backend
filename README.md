# Solution Creation

```bash
dotnet new sln --output <SolutionName>

mkdir src
```

# Project creation

1. Create the api under the src/<Microservice> folder

```bash
dotnet new webapi -n CourseManagementApi -o src/CourseManagement/CourseManagementApi
```

2. Add the project to the solution
```bash
dotnet sln DigitalMarketBackend.sln add src/CourseManagement/CourseManagementApi/CourseManagementApi.csproj --solution-folder src/CourseManagement
```

3. Create the architecture projects for the microservice
```bash
dotnet new classlib -n Domain -o src/CourseManagement/Domain
dotnet sln DigitalMarketBackend.sln add src/CourseManagement/Domain/Domain.csproj --solution-folder src/CourseManagement

dotnet new classlib -n Application -o src/CourseManagement/Application
dotnet sln DigitalMarketBackend.sln add src/CourseManagement/Application/Application.csproj --solution-folder src/CourseManagement

dotnet new classlib -n Persistance -o src/CourseManagement/Persistance
dotnet sln DigitalMarketBackend.sln add src/CourseManagement/Persistance/Persistance.csproj --solution-folder src/CourseManagement
```
