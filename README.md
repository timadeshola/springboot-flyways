# springboot-flyways
Demonstrating database migration in spring boot using flyways

Demonstrating database migration in spring boot using flyways

Spring Boot Database Migrations with Flyway

Flyway is a tool that lets you version control incremental changes to your database so that you can migrate it to a new version easily and confidently.

Here is a simple Spring Boot application with MySQL Database & Spring Data JPA showing how to use flyways for data migration.

Creating a Flyway Migration script
Flyway tries to read database migration scripts from classpath:db/migration folder by default.

All the migration scripts must follow a particular naming convention - V<VERSION_NUMBER>__<NAME>.sql. Checkout the Official Flyway documentation to learn more about naming convention.

How does Flyway manage migrations?
Flyway creates a table called flyway_schema_history when it runs the migration for the first time and stores all the meta-data required for versioning the migrations in this table.

Ensure you add this dependency to your pom.xml file
<plugin>
    <groupId>org.flywaydb</groupId>
    <artifactId>flyway-maven-plugin</artifactId>
    <version>4.0.3</version> 
</plugin>

Happy coding
