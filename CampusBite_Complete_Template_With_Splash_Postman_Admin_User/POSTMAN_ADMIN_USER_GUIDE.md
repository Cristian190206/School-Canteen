# CampusBite: Postman Admin and Student/User Testing

## Demo accounts
- Admin: `admin@campusbite.com` / `Admin123!`
- Student/User: `student@campusbite.com` / `Student123!`

These are development demo credentials; change them before any real deployment.

## Run the API
Open a terminal in `backend/CampusBiteAPI` and run:

```cmd
dotnet run --urls http://0.0.0.0:5133
```

Keep the API terminal open. If an older CampusBiteAPI instance is already running, stop it with Ctrl+C in its own terminal before restarting the updated version.

## Import into Postman
1. Open Postman and click **Import**.
2. Choose `postman/CampusBite_Admin_User.postman_collection.json`.
3. The collection's default `baseUrl` is `http://localhost:5133` for Postman on the laptop.

## Run requests in order
1. `1 - Health Check`
2. `2 - Login as Admin`
3. `3 - Admin: View Users (should show Admin and Student)`
4. `4 - Admin: Dashboard Summary`
5. `5 - Login as Student/User`
6. `6 - Student/User: View My Orders`

The login requests save their tokens automatically. Admin endpoints use `adminToken`; user endpoints use `userToken`. The admin users request should return both seeded demo accounts.

The startup code adds either demo account only if that email is missing, and does not delete existing users. Existing database records are preserved.
