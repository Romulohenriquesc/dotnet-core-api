# dotnet-core-api

# Creating project architecture

run 
dotnet new sln --name Api
dotnet new webapi -n application -o Api.Application --no-https
dotnet sln add .\Api.Application\
dotnet new classlib -n Domain -o Api.Domain -f netcoreapp3.1
dotnet sln add .\Api.Domain\
dotnet new classlib -n CrossCutting -f netcoreapp3.1 -o Api.CrossCutting
dotnet sln add .\Api.CrossCutting\
dotnet new classlib -n Data -f netcoreapp3.1 -o Api.Data
dotnet sln add .\Api.Data\
dotnet new classlib -n Service -f netcoreapp3.1 -o Api.Service
dotnet sln add .\Api.Service\
dotnet build

delete Class1.cs files

# Implementing entities and repositories
