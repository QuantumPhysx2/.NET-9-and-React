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
