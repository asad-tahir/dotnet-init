# DevApp
### A demo app in Clean Architecture with Blazor WebAssembly

dotnet ef commands for managing solution..
```
./
dotnet --info
dotnet new sln
dotnet new globaljson --sdk-version [version]
dotnet new gitignore
dotnet new editorconfig
touch README.md
echo # My Online Store > README.md

./src
dotnet new --list
dotnet new mvc -o DevApp.Web --use-program-main
dotnet new classlib -o DevApp.Core
dotnet new classlib -o DevApp.Infrastructure

./
dotnet sln add src/DevApp.Web/DevApp.Web.csproj
```

dotnet ef commands for managing database..
```
dotnet ef migrations add <name> -c AppDbContext -p src/DevApp.Infrastructure -s src/DevApp.Api -o Data/Migrations
dotnet ef migrations remove -c AppDbContext -p src/DevApp.Infrastructure -s src/DevApp.Api
dotnet ef database update -c AppDbContext -p src/DevApp.Infrastructure -s src/DevApp.Api
```
