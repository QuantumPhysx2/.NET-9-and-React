# .NET-9-and-React
How to setup a .NET 9 and above project with React as the frontend framework

# Procedure (React)
1. cd one directory into the root repository.
2. Run the command: npm create vite@latest "<app-name>.client"
3. Set "<appname>" as the package name.
4. Select React as the framework.
5. Select JavaScript as the variant.
6. cd into the Client directory
7. Run the command: npm install
8. Run the command: npm run dev

# Backend (DotNet)
1. cd one directory into the root repository.
2. Run the command: dotnet new web -n "<app-name>.server"

# Configuring the .Client and .Server Directories
(Client)
1. Create a file "<app-name>.Client.esproj".
2. Add the following code to the file:
```
  <Project Sdk="Microsoft.VisualStudio.JavaScript.Sdk/1.0.2752196">
    <PropertyGroup>
      <StartupCommand>npm run dev</StartupCommand>
      <JavaScriptTestRoot>src\</JavaScriptTestRoot>
      <JavaScriptTestFramework>Vitest</JavaScriptTestFramework>
      <!-- Allows the build (or compile) script located on package.json to run on Build -->
      <ShouldRunBuildScript>false</ShouldRunBuildScript>
      <!-- Folder where production build objects will be placed -->
      <BuildOutputFolder>$(MSBuildProjectDirectory)\dist</BuildOutputFolder>
    </PropertyGroup>
  </Project>
```
3. Save the changes.
4. (Visual Studio) Right click on the Visual Studio solution and add the .esproj file you created. This will load the front-end portion of the app.

(Server)
1. Open the "<app-name>.Server.csproj" file.
2. Add the following elements:
```
  <SpaRoot>..\NotMilestone.Client</SpaRoot>
  <SpaProxyLaunchCommand>npm run dev</SpaProxyLaunchCommand>
  <SpaProxyServerUrl>https://localhost:59722</SpaProxyServerUrl>
```
```
  <ItemGroup>
    <ProjectReference Include="..\NotMilestone.Client\NotMilestone.Client.esproj">
  	<ReferenceOutputAssembly>false</ReferenceOutputAssembly>
    </ProjectReference>
  </ItemGroup>
```
3. Install the package: Microsoft.AspNetCore.SpaProxy
4. Save the changes.
5. (Visual Studio) Reload the project for the backend portion of the app.

# Closing Notes
- You should now have a "Client" and "Server" folder to separate the stacks of the web app.
- (Linux) If npm is not installed, refer to this link: https://nodejs.org/en/download
- (Vite React) Refer to this link regarding Vite React: https://vite.dev/guide/#scaffolding-your-first-vite-project

# Troubleshooting
- If you get an error message from the CLI when using npm or yarn to create the frontend structure, error message "127" may appear. If this occurs, then the "esbuild.exe" file may be getting blocked from execution. Whitelist this .exe file to allow the package manager to complete the install and build stages of the frontend.
