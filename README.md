# SpringBoot_Lesson11

## Propmt for the Code Agent (Codex, Gemini Code Assistant or Copilot)

**Context**

I am working on a Spring Boot application (Spring Boot 3.3, Java 17) and want to add monitoring capabilities.

**Task**:

Configure the project to use Spring Boot Actuator and expose basic endpoints.

**Constraints**:

- Use Maven or Gradle for dependency management.

- The `health` and `info` endpoints must be exposed over the web.

- The `metrics` endpoint should NOT be exposed over the web.

- All actuator endpoints should be available under the path `/management` instead of the default `/actuator`.

**Steps**:

1.  Add the `spring-boot-starter-actuator` dependency to the build file.

2.  Modify the `application.properties` or `application.yml` file to:

    a. Change the base path for management endpoints to `/management`.
    
    b. Explicitly expose only the `health` and `info` endpoints.
    
3.  Provide the `curl` commands to verify the endpoints after running the application.

**Deliverables**:

- The Maven/Gradle dependency XML/Groovy snippet.

- The required lines for `application.properties`.

- `curl` commands to test `http://localhost:8080/management/health` and `http://localhost:8080/management/info`.

- `curl` command to verify that `http://localhost:8080/management/metrics` returns a 404 Not Found.

**Acceptance Criteria for your AI-generated code**:

•	The application compiles and runs with the new dependency.

•	Accessing /management/health returns a JSON response with "status": "UP".

•	Accessing /management/info returns an empty JSON object {}.

•	Accessing /management/metrics returns a 404 HTTP status.
