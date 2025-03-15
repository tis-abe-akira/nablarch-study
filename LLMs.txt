# Nablarch Framework Analysis and References

## Part 1: Framework Analysis

1. Overview
Nablarch is a Java application development and execution platform created by TIS for building mission-critical systems. It provides a comprehensive framework that integrates extensive experience in building mission-critical systems. The framework consists of execution control infrastructure for different processing methods (web, batch, etc.) and provides individual functionalities such as database access and validation.

1.1. Core Architecture
- Handler Queue based execution model
- Clear separation between execution infrastructure and business logic
- Modular design with pluggable components
- Support for multiple runtime platforms:
  * Web applications with HTML-based UI
  * RESTful Web Services
  * Batch processing (both Jakarta Batch and Nablarch native)
  * Messaging systems (MOM and DB-queue based)

2. Core Features
- Handler queue-based request processing architecture
- Built-in validation and type conversion capabilities
- Comprehensive domain validation support
- Rich set of standard library components
- Multiple batch processing approaches:
  * Jakarta Batch compliant processing
  * Nablarch native batch with database integration
  * DB-less batch processing
- Web application framework with JSP/Thymeleaf support
- RESTful API and HTTP messaging support
- Both synchronous and asynchronous messaging capabilities

3. Key Components

a) Handler Queue System
- Handler categories:
  * Common handlers (Global error, Thread context, etc.)
  * Web application specific handlers
  * Batch processing handlers
  * REST/Web service handlers
  * Database transaction handlers
- Security handlers:
  * CSRF protection
  * Authentication/Authorization
  * Input validation
- Resource management handlers:
  * Database connection
  * File handling
  * Message queues
- Standard handler implementations:
  * Request routing
  * Data format conversion
  * Validation processing
  * Transaction control
  * Multi-thread execution

b) Libraries
- Database access with transaction management
- Comprehensive file I/O operations
- Structured logging system
- Advanced validation framework
  * Bean validation
  * Domain validation
  * Cross-field validation
- Type conversion with normalization
- Code management system
- Authentication/Authorization

4. Architecture Principles
- Strict handler-based request processing
- Clear separation of concerns through modular design
- Support for both synchronous and asynchronous processing
- Comprehensive transaction management:
  * Database transaction control
  * Batch transaction handling
  * Messaging transaction support
- Thread safety by design
- No null collections (empty collections returned instead)
- English-standardized logs and messages
- Configurable SQL execution
- Minimal external dependencies

5. Development Support
- Comprehensive testing framework
  * Automated test support
  * Multi-thread testing limitations
  * Database testing utilities
- Development tools suite:
  * SQL Executor for database operations
  * DBA support tools
  * Code generators
- Maven-based project management
  * Archetype-based project generation
  * Multiple project templates
  * Dependency management
- Extensive blank project templates:
  * Web application templates
  * RESTful service templates
  * Batch application templates
  * Container-ready templates

6. Validation Features

6.1. Bean Validation (JSR-380)
- Standard constraint annotations
- Custom constraint definitions
- Group validation support
- Message interpolation
- Validation sequence definition
- Integration with JAX-RS
- Automatic validation in web apps

6.2. Nablarch Native Validation
- Domain-driven validation design:
  * Centralized validation rules
  * Type-safe domain definitions
  * Reusable validation patterns
  * Easy maintenance and updates
- Advanced features:
  * Pre-validation type conversion
  * Input value normalization
  * Cross-field validation rules
  * Database lookup validation
  * Custom validation rules
- Implementation options:
  * Annotation-based configuration
  * Programmatic validation
  * Custom validator development
  * Domain-specific validators

6.3. Form/Entity Validation
- Automatic form binding
- Entity validation support
- Validation result handling
- Custom message resolution
- Property name interpolation
- Validation groups support
- Error message customization

7. Best Practices
- Clear separation of handler responsibilities
- Preference for domain validation over individual annotations
- Proper transaction management:
  * Appropriate transaction boundaries
  * Error handling within transactions
  * Proper resource management
- Standardized error handling:
  * Global error handling
  * Business error management
  * System error processing
- Consistent logging practices:
  * Structured log formats
  * Performance logging
  * Operation logging
  * Monitoring support

8. Limitations and Considerations
- Testing framework limitations:
  * No multi-thread testing support
  * Limited Jakarta Batch testing capabilities
- Batch processing considerations:
  * Potential delays in resident batch processing
  * Recommendation to use DB queue messaging for certain scenarios
- SQL execution constraints:
  * No support for WITH clause
  * IN clause limitations
  * DATETIME literal restrictions
- Java compatibility:
  * Java 17 compliance
  * Special considerations for Java 21
  * Container deployment requirements

9. Development Tools and Utilities
- SQL Executor:
  * Interactive SQL execution
  * Support for Nablarch SQL syntax
  * Multiple database support
  * Real-time execution feedback
  * Transaction management
  * Query optimization support
- Testing Framework:
  * Unit test support
  * Automated test framework
  * Test tools for development
  * Database testing utilities
  * Mock object support
- Build and Deployment:
  * Maven plugins
  * Container support
  * Database management tools
  * Migration utilities
  * Environment configuration

10. Project Structure and Organization
- Module-based architecture:
  * Core framework modules
  * Extension modules
  * Application modules
  * Custom project modules
- Layered architecture patterns:
  * Presentation layer
  * Business logic layer
  * Data access layer
  * Common utilities layer
- Application type support:
  * Web applications (JSP/Thymeleaf)
  * Batch applications (Jakarta/Native)
  * RESTful services
  * Messaging systems (MOM/DB)
- Container deployment support:
  * Docker container support
  * Cloud-ready architecture
  * Scalability considerations
  * Monitoring integration
  * Security compliance

## Part 2: Documentation References

### Source Documentation
Primary Documentation: https://nablarch.github.io/docs/LATEST/doc/
English Documentation: https://nablarch.github.io/docs/LATEST/doc/en/

### Core Documentation References

1. Overview and Architecture
- Main Overview: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/nablarch/index.html
- Architecture Details: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/nablarch/architecture.html
- Big Picture: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/nablarch/big_picture.html

2. Application Types
- Web Applications: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/web/index.html
- Batch Applications: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/batch/nablarch_batch/index.html
- RESTful Web Services: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/web_service/rest/index.html
- HTTP Messaging: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/web_service/http_messaging/index.html

3. Validation Framework
- Bean Validation: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/validation/bean_validation.html
- Nablarch Validation: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/validation/nablarch_validation.html
- Input Value Check: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/validation.html

4. Database and Data Access
- Database Library: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/database/index.html
- Database Management: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/database/database.html
- Universal DAO: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/database/universal_dao.html
- Transaction Management: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/handlers/common/transaction_management_handler.html

5. Security Features
- Authentication: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/authentication.html
- Authorization: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/authorization.html
- CSRF Protection: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/handlers/web/csrf_token_verification_handler.html
- Password Encryption: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/password_encryption.html

6. Development Tools
- SQL Executor: https://nablarch.github.io/docs/LATEST/doc/en/development_tools/toolbox/SqlExecutor/SqlExecutor.html
- Testing Framework: https://nablarch.github.io/docs/LATEST/doc/en/development_tools/testing_framework/index.html
- JSP Static Analysis: https://nablarch.github.io/docs/LATEST/doc/en/development_tools/toolbox/JspStaticAnalysis/01_JspStaticAnalysis.html
- Database Tools: https://nablarch.github.io/docs/LATEST/doc/en/development_tools/toolbox/index.html

7. Handler References
- Common Handlers: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/handlers/common/index.html
- Web Handlers: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/handlers/web/index.html
- Batch Handlers: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/handlers/batch/index.html
- REST Handlers: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/handlers/rest/index.html

8. Messaging and Integration
- Messaging Overview: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/messaging/index.html
- Email Integration: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/libraries/mail.html
- HTTP Messaging: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/web_service/http_messaging/architecture.html
- Database Messaging: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/messaging/db/index.html

9. Getting Started Guides
- Web Application: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/web/getting_started/index.html
- REST Services: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/web_service/rest/getting_started/index.html
- Batch Processing: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/batch/nablarch_batch/getting_started/getting_started.html
- Blank Project: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/blank_project/index.html

10. Example Applications and Code
Main Examples Repository: https://nablarch.github.io/docs/LATEST/doc/en/examples/index.html
- Web Example: https://github.com/nablarch/nablarch-example-web
- REST Example: https://github.com/nablarch/nablarch-example-rest
- Batch Example: https://github.com/nablarch/nablarch-example-batch
- Messaging Example: https://github.com/nablarch/nablarch-example-mom
- HTTP Messaging: https://github.com/nablarch/nablarch-example-http-messaging
- DB Messaging: https://github.com/nablarch/nablarch-example-db-queue

11. Additional Resources
- API Documentation: https://nablarch.github.io/docs/6u2/javadoc/
- Maven Repository: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/blank_project/maven.html
- Migration Guides: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/blank_project/ModifySettings.html

## Limitations and Known Issues
Documentation Link: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/nablarch/policy.html

1. Testing Framework Limitations
- No multi-thread testing support
- Limited Jakarta Batch testing capabilities
Reference: https://nablarch.github.io/docs/LATEST/doc/en/development_tools/testing_framework/index.html

2. SQL Executor Constraints
- No support for WITH clause
- IN clause limitations
- DATETIME literal restrictions
Reference: https://nablarch.github.io/docs/LATEST/doc/en/development_tools/toolbox/SqlExecutor/SqlExecutor.html

3. Java Compatibility
- Java 17 compliance required
- Special considerations for Java 21
Reference: https://nablarch.github.io/docs/LATEST/doc/en/application_framework/application_framework/nablarch/policy.html#compliant-with-java17
