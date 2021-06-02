<h1 class="code-line" data-line-start=0 data-line-end=1 ><a id="dotnetcoreapi_0"></a>dotnet-core-api</h1>

<h3 class="code-line" data-line-start=2 data-line-end=3 ><a id="Packages_2"></a>Packages</h3>
<p class="has-line-data" data-line-start="3" data-line-end="5">Microsoft.EntityFrameworkCore: 3.1.409<br>
Pomelo.EntityFrameworkCore.MySql: 3.1.2</p>

<h2 class="code-line" data-line-start=2 data-line-end=3 ><a id="Creating_project_architecture_2"></a>Creating project architecture</h2>
<p class="has-line-data" data-line-start="4" data-line-end="17">run commands<br>
dotnet new sln --name Api<br>
dotnet new webapi -n application -o Api.Application --no-https<br>
dotnet sln add .\Api.Application<br>
dotnet new classlib -n Domain -o Api.Domain -f netcoreapp3.1<br>
dotnet sln add .\Api.Domain<br>
dotnet new classlib -n CrossCutting -f netcoreapp3.1 -o Api.CrossCutting<br>
dotnet sln add .\Api.CrossCutting<br>
dotnet new classlib -n Data -f netcoreapp3.1 -o Api.Data<br>
dotnet sln add .\Api.Data<br>
dotnet new classlib -n Service -f netcoreapp3.1 -o Api.Service<br>
dotnet sln add .\Api.Service<br>
dotnet build</p>
<p class="has-line-data" data-line-start="18" data-line-end="19">delete Class1.cs files</p>
<h2 class="code-line" data-line-start=20 data-line-end=21 ><a id="Implementing_entities_and_repositories_20"></a>Implementing entities and repositories</h2>
