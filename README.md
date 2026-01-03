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

# Closing Notes
- You should now have a "Client" and "Server" folder to separate the stacks of the web app.
- (Linux) If npm is not installed, refer to this link: https://nodejs.org/en/download
- (Vite React) Refer to this link regarding Vite React: https://vite.dev/guide/#scaffolding-your-first-vite-project

# Troubleshooting
- If you get an error message from the CLI when using npm or yarn to create the frontend structure, error message "127" may appear. If this occurs, then the "esbuild.exe" file may be getting blocked from execution. Whitelist this .exe file to allow the package manager to complete the install and build stages of the frontend.
