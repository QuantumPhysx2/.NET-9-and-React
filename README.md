# .NET-9-and-React
How to setup a .NET 9 and above project with React as the frontend framework

# Pre-text
Follow this guide if you are starting from complete scratch:
- Visual Studio > ASP.NET Core Empty project
- Adding the React frontend framework in a separate instance after creating the .sln
- You are using Vite instead of the old Create-React-App (CRA). CRA is deprecated as of FEB 2025

# Procedure (React)
1. cd into the project directory
2. Run the command: npm create vite@latest clientapp -- --template react
3. Select React as the framework.
4. Select JavaScript as the variant (or of personal choice).
5. cd into the clientapp directory
6. Run the command: npm install
7. Run the command: npm run dev

Outcome: you will now have the latest version of the React directory called "clientapp".

This completes adding the React frontend to your project.
