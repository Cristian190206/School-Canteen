# CampusBite Complete Template

Includes separate HTML pages, shared CSS/JS, ASP.NET Core 10 REST API, and SQLite database initialization.

## Run backend
1. Install .NET 10 SDK.
2. Open terminal in `backend/CampusBiteAPI`.
3. Run `dotnet restore`, then `dotnet run`.
4. API default URL: http://localhost:5133. SQLite database is created automatically.

## Run frontend
Open `frontend` with VS Code Live Server (port 5500), then open `splash.html` for the landing page, or `login.html` to go directly to sign in.
If the API URL differs, edit `frontend/js/config.js`.

Demo accounts:
- Student: student@campusbite.com / Student123!
- Admin: admin@campusbite.com / Admin123!

Classroom starter only. Change demo passwords and improve token security before production.


## Postman: Admin and Student/User

Import `postman/CampusBite_Admin_User.postman_collection.json` and follow `POSTMAN_ADMIN_USER_GUIDE.md`. Demo accounts: `admin@campusbite.com` / `Admin123!` and `student@campusbite.com` / `Student123!`.
