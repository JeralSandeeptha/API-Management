# API Gateway

## What is a Software API Gateway?

An API Gateway is a single entry point that sits between clients (frontend, mobile apps) and your backend services (APIs).

Instead of:
```bash
Frontend → Spring Boot API
Frontend → Node API
Frontend → .NET API
Frontend → Django API
```

You do:
```bash
Frontend → API Gateway → Backend APIs
```

The gateway forwards requests to the correct service.

<br />

## What Does an API Gateway Do?

#### 1️⃣ Routing

Decides which backend service should handle the request.

```
/users → Spring Boot
/orders → .NET
/analytics → Node.js
```

#### 2️⃣ Authentication & Authorization

Validates JWT tokens before forwarding requests.

```
Checks if token is valid
Checks user roles
```

#### 3️⃣ Rate Limiting

Prevents abuse.

```
100 requests per minute per user
```

#### 4️⃣ Logging & Monitoring

Tracks API usage.

#### 5️⃣ CORS Handling

Manages cross-origin requests.

#### 6️⃣ Request / Response Transformation

Modify request format before sending to backend.

<br />

## What is API Gateway Management?

Now this is different.

API Gateway Management means the tools and systems used to:**

- Create APIs
- Secure APIs
- Monitor APIs
- Version APIs
- Publish APIs
- Analyze usage
- Control access

It’s the administrative layer around APIs.

## Example Platforms

Here are popular API Gateway & Management solutions:

- Google Cloud Platform – API Gateway & Apigee
- Amazon Web Services – API Gateway
- Microsoft Azure – Azure API Management
- Kong – Kong Gateway
- NGINX – NGINX API Gateway

## Difference Between API Gateway and API Management

| API Gateway                | API Management                       |
| -------------------------- | ------------------------------------ |
| Technical component        | Business + technical platform        |
| Handles request routing    | Handles lifecycle of APIs            |
| Focused on traffic control | Focused on governance                |
| Runs at runtime            | Includes analytics, developer portal |
