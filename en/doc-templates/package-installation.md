## Installation

It is suggested to use the [ABP CLI](CLI.md) to install this package.
{{if UI == "NG"}} -u angular{{end}}{{if DB == "Mongo"}} -d mongodb{{end}}{{if Tiered == "Yes"}} --tiered{{end}}

### Using the ABP CLI

Open a command line window in the folder of the project (.csproj file) and type the following command:

````bash
abp add-package {{PackageName}}
````

### Manual Installation 

If you want to manually install;

1. Add the [{{ PackageName }}](https://www.nuget.org/packages/{{ PackageName }}) NuGet package to your project:

   ````
   Install-Package {{ PackageName }}
   ````

2.  Add the `{{ ModuleClassName }}` to the dependency list of your module:

````csharp
[DependsOn(
    //...other dependencies
    typeof({{ ModuleClassName }}) //Add the module
    )]
public class YourModule : AbpModule
{
}
````