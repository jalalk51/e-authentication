# E-Auth System Agent Instructions

## Build and Run
- Use `docker-compose up --build` to start all services.
- For local development, run `node server.js` in each service directory.

## Architecture
- Microservices: API Gateway routes to auth-service and user-service.
- Auth-service handles OTP and JWT; user-service is a stub.
- Frontend is vanilla JS served by Nginx.

## Conventions
- Use `verifyToken` middleware for protected routes.
- Responses follow `{ success: bool, message?: string, ...data }` format.
- Console logging with emojis for debugging.

## Pitfalls
- OTP codes are logged to console, not sent.
- Hardcoded secrets; no environment variables.
- Tokens not persisted; lost on refresh.

## File Exclusions
- Exclude `node_modules` directories from code searches and edits.
- Ignore log files and temporary files.

See [API_DOCS.md](API_DOCS.md) for endpoint details.