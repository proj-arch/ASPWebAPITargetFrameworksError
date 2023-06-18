# ASPWebAPITargetFrameworksError
Demonstrates the error that occurs when using the package 'Swashbuckle.AspNetCore' in combination with the tag TargetFrameworks (plural) in the project file.

Issue https://github.com/dotnet/aspnetcore/issues/40577

### Remarks
- Typically you would use TargetFrameworks (plural) when you want to target multiple frameworks. But sind the error also occurs with one target framework, this project states net6.0 only for simplicity reasons.
In reality the reason for using the plural TargetFrameworks tag is because I want to target multiple frameworks.
- The project works fine as long as I stick to tag TargetFramework (singular).
It also seems to work when I remove the PackageReference to Swashbuckle.AspNetCore and all its usages. But that removes OpenAPI support obviously.

### Steps
1. clone the repo
2. load the TestAPI.sln in Visual Studio 2022
3. try to build the solution
3. you will get 2 errors
