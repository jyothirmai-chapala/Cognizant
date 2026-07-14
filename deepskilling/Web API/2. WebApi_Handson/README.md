# Lab 2 – ASP.NET Core Web API with Swagger and Postman

## Experiment Title
ASP.NET Core Web API using Swagger and Postman

---

# Aim

To create an ASP.NET Core Web API, test API endpoints using Swagger UI and Postman, and understand API routing using Route attributes.

---

# Objectives

- Create an ASP.NET Core Web API project.
- Enable Swagger (OpenAPI) support.
- Execute API methods using Swagger UI.
- Test API endpoints using Postman.
- Create a custom Employee API.
- Modify the Route attribute and verify the updated endpoint.

---

# Software Requirements

- Visual Studio 2022
- .NET 10 SDK
- ASP.NET Core Web API
- Swagger UI
- Postman

---

# Project Created

Project Name:

```
FirstWebAPI
```

---

# Files Used

```
Program.cs
EmployeeController.cs
WeatherForecastController.cs
appsettings.json
launchSettings.json
```

---

# Procedure

## Step 1: Create Web API Project

- Open Visual Studio.
- Create a new **ASP.NET Core Web API** project.
- Select **Authentication: None**.
- Enable **OpenAPI Support**.
- Enable **Use Controllers**.
- Create the project.

---

## Step 2: Run the Application

- Build and run the project.
- Swagger UI opens automatically in the browser.
- Verified the default **WeatherForecast** API.

---

## Step 3: Test Default API

Executed the following endpoint:

```
GET /WeatherForecast
```

Verified:

- JSON response
- HTTP Status Code 200 (OK)

---

## Step 4: Test API using Postman

- Installed Postman Desktop Application.
- Created a GET request.

Request URL

```
https://localhost:7272/WeatherForecast
```

Clicked **Send**.

Verified:

- JSON Response
- Status Code: 200 OK

---

## Step 5: Create Employee Controller

Created a new API Controller named:

```
EmployeeController
```

Added a GET action that returns a list of employees.

Example Output

```json
[
    "John",
    "David",
    "Alice",
    "Robert"
]
```

---

## Step 6: Test Employee API

Executed

```
GET /Employee
```

using

- Swagger UI
- Postman

Verified successful JSON response.

---

## Step 7: Modify Route

Changed the Route attribute from

```csharp
[Route("[controller]")]
```

to

```csharp
[Route("Emp")]
```

The API endpoint changed from

```
/Employee
```

to

```
/Emp
```

---

## Step 8: Test Modified Route

Executed

```
GET /Emp
```

using Swagger and Postman.

Verified successful execution with HTTP Status Code **200 OK**.

---

# Output

Successfully tested the following APIs.

### WeatherForecast API

```
GET /WeatherForecast
```

### Employee API

```
GET /Employee
```

### Modified Route

```
GET /Emp
```

All APIs returned JSON responses successfully.

---

# Result

Successfully created an ASP.NET Core Web API application, enabled Swagger support, tested APIs using Swagger UI and Postman, created a custom Employee API, modified the Route attribute, and verified the updated endpoint successfully.

---

# Conclusion

The experiment was completed successfully. We learned how to create an ASP.NET Core Web API, test endpoints using Swagger and Postman, create custom controllers, and modify API routes using Route attributes.
