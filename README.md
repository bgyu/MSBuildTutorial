# MSBuild Tutorial
This is a tutorial for MSBuild, namely Microsoft Build Engine, is a platform for building applications. It is using XML to control the build process.

## Hello World
### Most Basic Project structure
```xml
<?xml version="1.0" encoding="utf-8"?> 
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003"> 
</Project> 
```
- Project: Define a top level project node.
  * DefaultTargets: Attribute used to define your build targets, more targes are separated by semi-colon(;)
- Target: Define your target. 
  * Name: Attribute used to define target name.  Can define multiple targes.
- PropertyGroup: Define properties used in your build process. 
  Can view it as a list of global variables. Use $(PropertyName) to refer to a property.
- Message: Predefined task. Shows a build message.
 * Text: attribute used for message text.

### How to build
```bash
MSBuild Hello.proj
```
* If only have one project, then can skip `Hello.proj`
* target: specify which target to build
```bash
MSBuild -target:Go Hello.proj
```
