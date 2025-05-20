# Regression
[![Build Status](https://github.com/kenya-jug/regression/actions/workflows/maven.yml/badge.svg)](https://github.com/kenya-jug/regression/actions/workflows/maven.yml)

A Spring Boot server for collecting, storing, and analyzing error logs with REST APIs and AI-powered log analysis

### **Regression – Requirements Specification**

![Project Overview Diagram](/specification/assets/diagram.png)

**Overview:**
**Regression** is a Spring Boot-based server for collecting, storing, and analyzing application error logs. It provides RESTful APIs for log ingestion and retrieval, with AI-driven analysis to detect anomalies, trends, and root causes.


---

<img width="1184" alt="Screenshot 2025-05-20 at 15 32 17" src="https://github.com/user-attachments/assets/b32085f6-4d35-4e35-9ad9-7dae4a27f532" />

---

https://github.com/user-attachments/assets/50589dbc-0b7f-4536-a047-e82c18b078d5

---

### Prerequisites

- Java 21 or higher
- Maven 3.8 or higher
- SQLite 3 (or your preferred database)
- Docker (optional, for containerized deployment)

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/kenya-jug/regression.git
   cd regression
   ```

2. **Configure the database**
   - SQLite database will be automatically created in the project directory
   - Update `src/main/resources/application.properties` with your database configuration:
     ```properties
     spring.datasource.url=jdbc:sqlite:regression.db
     spring.datasource.driver-class-name=org.sqlite.JDBC
     ```

3. **Build the project**
   ```bash
   mvn clean install
   ```

4. **Run the application**
   ```bash
   mvn spring-boot:run
   ```
   The server will start on `http://localhost:8080`

### Docker Deployment

1. **Build the Docker image**
   ```bash
   docker build -t regression .
   ```

2. **Run the container**
   ```bash
   docker run -p 8080:8080 regression
   ```

### API Documentation

Once the application is running, you can access the API documentation at:
- Swagger UI: `http://localhost:8080/swagger-ui.html`
- OpenAPI Specification: `http://localhost:8080/v3/api-docs`

### Environment Variables

The following environment variables can be configured:

| Variable | Description | Default |
|----------|-------------|---------|
| `SERVER_PORT` | Port to run the application | 8080 |
| `SPRING_PROFILES_ACTIVE` | Active Spring profile | dev |
| `JWT_SECRET` | Secret key for JWT tokens | (required in production) |

### Troubleshooting

- If you encounter database issues, ensure you have write permissions in the project directory
- For port conflicts, change the `SERVER_PORT` environment variable
- Check the application logs for detailed error messages

### Development Workflow

1. **Running Tests**
   ```bash
   mvn test
   ```

2. **Code Style Check**
   ```bash
   mvn checkstyle:check
   ```

3. **Generating Documentation**
   ```bash
   mvn javadoc:javadoc
   ```

### Contributing

1. Create a new branch for your feature
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes and commit them
   ```bash
   git add .
   git commit -m "Description of your changes"
   ```

3. Push your changes and create a pull request

### Support

For additional help or questions:
- Open an issue on GitHub
- Check the [Wiki](https://github.com/kenya-jug/regression/wiki) for detailed documentation
- Join our [Discord community](https://discord.gg/kenya-jug)

## Description
This PR addresses issue #16 by adding a comprehensive setup guide to the README.md file. The changes provide clear instructions for developers to set up and run the project locally.

## Changes Made
- Added **Prerequisites** section listing required software and tools
- Added **Local Development Setup** with step-by-step instructions:
  - Repository cloning
  - Database configuration
  - Build process
  - Running the application
- Added **Docker Deployment** instructions
- Added **API Documentation** access information
- Added **Environment Variables** configuration table
- Added **Troubleshooting** section for common issues
- Added **Development Workflow** section covering:
  - Running tests
  - Code style checks
  - Documentation generation
- Added **Contributing** guidelines
- Added **Support** section with community resources

## Testing
- [x] Verified all code blocks render correctly in GitHub
- [x] Tested all commands in the guide
- [x] Ensured proper formatting and markdown syntax

## Related Issues
Closes #16

## Screenshots
N/A - Documentation changes only

## Additional Notes
- The setup guide follows best practices for Spring Boot applications
- Instructions are clear and suitable for both new and experienced developers
- Added both local development and Docker deployment options




















































































<!-- coverage start -->
## 📊 Code Coverage Report

**Overall Coverage: 100.00% ✅**

| Metric      | Covered | Missed | Total | Coverage  |
|-------------|---------|--------|-------|-----------|
| INSTRUCTION | 3524    | 0      | 3524  | 100.00% ✅ |
| LINE        | 858     | 0      | 858   | 100.00% ✅ |
| BRANCH      | 88      | 0      | 88    | 100.00% ✅ |
| METHOD      | 184     | 0      | 184   | 100.00% ✅ |
| CLASS       | 36      | 0      | 36    | 100.00% ✅ |
| COMPLEXITY  | 229     | 0      | 229   | 100.00% ✅ |
<!-- coverage end -->
