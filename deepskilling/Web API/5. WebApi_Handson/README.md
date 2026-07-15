# EXPERIMENT – 5
# JWT Authentication and Authorization in ASP.NET Core Web API

## Aim
To implement JWT (JSON Web Token) based authentication and authorization in an ASP.NET Core Web API and test the secured APIs using Swagger and Postman.

---

## Objective

- Understand the concept of JWT Authentication.
- Configure JWT Authentication in ASP.NET Core Web API.
- Generate JWT Tokens using an Auth Controller.
- Secure API endpoints using the Authorize attribute.
- Access secured APIs using Bearer Token in Postman.
- Verify Unauthorized (401) response for invalid or missing tokens.
- Understand JWT expiration and Role-Based Authorization.

---

## Theory

JWT (JSON Web Token) is a secure way to authenticate users without maintaining server-side sessions.

A JWT consists of three parts:

1. Header
2. Payload (Claims)
3. Signature

After successful authentication, the server generates a JWT token and sends it to the client. The client includes this token in the Authorization header for every protected API request.

Format:

Authorization: Bearer <JWT Token>

The server validates the token before allowing access to protected resources.

---

## Software Requirements

- Visual Studio 2022
- .NET 8 Web API
- Swagger UI
- Postman Desktop
- Microsoft.AspNetCore.Authentication.JwtBearer NuGet Package

---

## Implementation

### Step 1: Configure JWT Authentication

Configured JWT Authentication inside Program.cs by:

- Adding Authentication Service.
- Configuring JwtBearer Authentication.
- Setting:
  - Secret Key
  - Issuer
  - Audience
- Enabling Authentication Middleware.

---

### Step 2: Create AuthController

Created a new controller named **AuthController**.

Implemented:

- GenerateJSONWebToken() method
- GET API (/Auth)

The API generates a JWT Token containing:

- UserId Claim
- Role Claim (Admin)

The token is signed using a Secret Key and returned to the client.

---

### Step 3: Secure EmployeeController

Protected EmployeeController using:

```csharp
[Authorize]
