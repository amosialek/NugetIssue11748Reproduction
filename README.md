# NugetIssue11748Reproduction
Minimal project for reproduction of https://github.com/NuGet/Home/issues/11748

Steps to reproduce:
 - open in VS 17.3.2 or later
 - try to build (fails)
 - remove `<PackageVersion Include="System.Resources.Extensions" Verison="6.0.0" />` from `Directory.Packages.props` 
 - try to build (success)
 - add `<PackageVersion Include="System.Resources.Extensions" Verison="6.0.0" />` to `Directory.Packages.props` 
 - try to build (success)
 - close VS, remove `bin/`, `obj/` and `.vs/` folders
 - open solution again and try to build (fails)
