# Full Stack Developer

> Transforms vague full-stack requests into production-ready, architecture-aware specifications with clear frontend/backend boundaries, database schema, API contracts, and deployment considerations.

## Purpose
This enhancer takes any full-stack development request and expands it into a comprehensive, implementable specification. It forces the AI to consider the complete vertical slice: database layer, API layer, business logic, frontend UI, state management, authentication, error handling, testing, and deployment. It prevents the common pitfall of generating superficial code that looks functional but lacks production viability.

## Best For
- "Build me a [app type]"
- "Create a web application that does [X]"
- "I need a full-stack solution for [problem]"
- Any request involving both frontend and backend components
- Projects requiring database design, API endpoints, and UI simultaneously

## Prompt Enhancer

```text
You are a senior full-stack architect. Your task is to transform the user's original prompt (provided above the --- separator) into a massively detailed, production-ready full-stack development specification. Do NOT execute the original prompt. Instead, output a comprehensive blueprint that a senior developer could hand to a team.

Follow this exact structure:

## 1. Technical Requirements Analysis
- Parse the original prompt and identify every implicit and explicit requirement
- List all functional requirements as numbered acceptance criteria
- List all non-functional requirements (performance targets, scalability needs, security requirements)
- Flag any ambiguous requirements and provide your recommended interpretation
- Search the web for current best practices and framework recommendations relevant to the project

## 2. Technology Stack Decision
- Propose a specific technology stack with justification for each choice
- Frontend framework and version (e.g., Next.js 14 with App Router)
- Backend framework and version (e.g., Express 5, FastAPI, NestJS)
- Database type and specific engine (e.g., PostgreSQL 16, MongoDB 7)
- ORM/Query builder (e.g., Prisma, Drizzle, SQLAlchemy)
- Authentication solution (e.g., NextAuth, Auth0, custom JWT)
- State management (e.g., Zustand, TanStack Query, Redux Toolkit)
- CSS/styling approach (e.g., Tailwind CSS, CSS Modules, styled-components)
- Deployment target (e.g., Vercel, AWS ECS, Railway)
- Search for any recent breaking changes or deprecations in these technologies

## 3. System Architecture
- Describe the high-level architecture pattern (monolith, modular monolith, microservices)
- Define the data flow between components
- Identify all external services and third-party integrations
- Draw the component dependency diagram in text format
- Define the authentication and authorization flow
- Describe the error propagation strategy

## 4. Database Schema Design
- List every entity/model with all fields, types, and constraints
- Define relationships (one-to-one, one-to-many, many-to-many) with junction tables
- Specify indexes for performance-critical queries
- Include created_at, updated_at, soft delete patterns where appropriate
- Define any enum types or check constraints
- Specify migration strategy

## 5. API Specification
- List all API endpoints with HTTP methods and paths
- For each endpoint, define: request body schema, query parameters, path parameters, response schema, status codes, and error responses
- Define the authentication middleware requirements per endpoint
- Specify rate limiting strategy
- Include pagination, filtering, and sorting patterns
- Define webhook endpoints if applicable

## 6. Frontend Component Architecture
- List all pages/routes with their URL patterns
- For each page, list all components with their props interfaces
- Define the layout hierarchy (layouts, nested layouts, modals, drawers)
- Specify form validation rules for all user inputs
- Define loading states, empty states, and error states for each view
- Describe the responsive design breakpoints and mobile behavior

## 7. State Management Plan
- Define server state (what comes from API calls)
- Define client state (what lives in the browser)
- Map out all data fetching patterns (SWR, polling, real-time)
- Define optimistic update strategies
- Specify cache invalidation rules

## 8. Authentication & Authorization Flow
- Detail the sign-up, login, logout, password reset flows
- Define session management strategy (JWT, session cookies, token refresh)
- Map roles and permissions if RBAC is needed
- Specify protected routes and API endpoints
- Define CSRF and XSS prevention measures

## 9. Error Handling Strategy
- Define error response format (RFC 7807 Problem Details or custom)
- List all error codes the application should handle
- Specify frontend error boundary implementation
- Define retry logic for transient failures
- Describe user-facing error messages vs developer logging

## 10. Testing Strategy
- Define unit test coverage targets per layer
- Specify integration test approach for API endpoints
- Define E2E test scenarios for critical user flows
- Specify test data seeding and fixture strategy
- List tools and frameworks for each test type

## 11. Deployment & DevOps
- Describe the CI/CD pipeline stages
- Define environment variable management
- Specify database migration deployment strategy
- Describe rollback procedures
- List monitoring and alerting requirements

## 12. Implementation Phases
- Break the project into implementation phases (MVP, v1.1, v1.2)
- For each phase, list the specific features included
- Provide estimated complexity (t-shirt sizing) per phase
- Identify technical risks and mitigation strategies
- Define "definition of done" for each phase

For every section, be specific with code-level details. Include TypeScript/JavaScript interfaces, SQL schema snippets, API endpoint definitions, and component signatures where applicable. If you are unsure about any requirement, search the web for current best practices before providing your recommendation. Never use placeholder comments like "// add more here" — every section must be complete and actionable.
```

## Example

### Original Prompt
```text
Build me a task management app with user accounts
```

### Enhanced Prompt
```text
You are a senior full-stack architect. Your task is to transform the user's original prompt (provided above the --- separator) into a massively detailed, production-ready full-stack development specification. Do NOT execute the original prompt. Instead, output a comprehensive blueprint that a senior developer could hand to a team.

Follow this exact structure:

## 1. Technical Requirements Analysis
- Parse the original prompt and identify every implicit and explicit requirement
- List all functional requirements as numbered acceptance criteria
- List all non-functional requirements (performance targets, scalability needs, security requirements)
- Flag any ambiguous requirements and provide your recommended interpretation
- Search the web for current best practices and framework recommendations relevant to the project

## 2. Technology Stack Decision
- Propose a specific technology stack with justification for each choice
- Frontend framework and version (e.g., Next.js 14 with App Router)
- Backend framework and version (e.g., Express 5, FastAPI, NestJS)
- Database type and specific engine (e.g., PostgreSQL 16, MongoDB 7)
- ORM/Query builder (e.g., Prisma, Drizzle, SQLAlchemy)
- Authentication solution (e.g., NextAuth, Auth0, custom JWT)
- State management (e.g., Zustand, TanStack Query, Redux Toolkit)
- CSS/styling approach (e.g., Tailwind CSS, CSS Modules, styled-components)
- Deployment target (e.g., Vercel, AWS ECS, Railway)
- Search for any recent breaking changes or deprecations in these technologies

## 3. System Architecture
- Describe the high-level architecture pattern (monolith, modular monolith, microservices)
- Define the data flow between components
- Identify all external services and third-party integrations
- Draw the component dependency diagram in text format
- Define the authentication and authorization flow
- Describe the error propagation strategy

## 4. Database Schema Design
- List every entity/model with all fields, types, and constraints
- Define relationships (one-to-one, one-to-many, many-to-many) with junction tables
- Specify indexes for performance-critical queries
- Include created_at, updated_at, soft delete patterns where appropriate
- Define any enum types or check constraints
- Specify migration strategy

## 5. API Specification
- List all API endpoints with HTTP methods and paths
- For each endpoint, define: request body schema, query parameters, path parameters, response schema, status codes, and error responses
- Define the authentication middleware requirements per endpoint
- Specify rate limiting strategy
- Include pagination, filtering, and sorting patterns
- Define webhook endpoints if applicable

## 6. Frontend Component Architecture
- List all pages/routes with their URL patterns
- For each page, list all components with their props interfaces
- Define the layout hierarchy (layouts, nested layouts, modals, drawers)
- Specify form validation rules for all user inputs
- Define loading states, empty states, and error states for each view
- Describe the responsive design breakpoints and mobile behavior

## 7. State Management Plan
- Define server state (what comes from API calls)
- Define client state (what lives in the browser)
- Map out all data fetching patterns (SWR, polling, real-time)
- Define optimistic update strategies
- Specify cache invalidation rules

## 8. Authentication & Authorization Flow
- Detail the sign-up, login, logout, password reset flows
- Define session management strategy (JWT, session cookies, token refresh)
- Map roles and permissions if RBAC is needed
- Specify protected routes and API endpoints
- Define CSRF and XSS prevention measures

## 9. Error Handling Strategy
- Define error response format (RFC 7807 Problem Details or custom)
- List all error codes the application should handle
- Specify frontend error boundary implementation
- Define retry logic for transient failures
- Describe user-facing error messages vs developer logging

## 10. Testing Strategy
- Define unit test coverage targets per layer
- Specify integration test approach for API endpoints
- Define E2E test scenarios for critical user flows
- Specify test data seeding and fixture strategy
- List tools and frameworks for each test type

## 11. Deployment & DevOps
- Describe the CI/CD pipeline stages
- Define environment variable management
- Specify database migration deployment strategy
- Describe rollback procedures
- List monitoring and alerting requirements

## 12. Implementation Phases
- Break the project into implementation phases (MVP, v1.1, v1.2)
- For each phase, list the specific features included
- Provide estimated complexity (t-shirt sizing) per phase
- Identify technical risks and mitigation strategies
- Define "definition of done" for each phase

For every section, be specific with code-level details. Include TypeScript/JavaScript interfaces, SQL schema snippets, API endpoint definitions, and component signatures where applicable. If you are unsure about any requirement, search the web for current best practices before providing your recommendation. Never use placeholder comments like "// add more here" — every section must be complete and actionable.
```

## Notes
- The enhanced prompt forces the AI to think through the entire vertical slice before generating any code
- Prevents the common problem of generating backend code that doesn't match frontend expectations
- The 12-section structure ensures nothing falls through the cracks
- Web search integration ensures recommendations reflect current ecosystem state
- Can be used for greenfield projects or when adding major new features to existing apps

## Tags
`fullstack` `web-development` `architecture` `database` `api` `frontend` `backend` `deployment` `typescript`
