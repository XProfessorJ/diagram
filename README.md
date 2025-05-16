h1. TIBCO Migration Utility Documentation

h2. 1. Tool Overview
The *TIBCO Migration Utility* is designed to streamline the migration of TIBCO process files to Java-based microservices. It automates the conversion of complex TIBCO XML configurations, XSD schemas, and copybook files into a standardized Java format, improving development efficiency and reducing manual errors.

---

h2. 2. Key Features

* Automated conversion of TIBCO process files
* Support for XSD schema and copybook parsing
* Highly customizable through property files
* Seamless integration with existing CI/CD pipelines
* Detailed logging for efficient debugging

---

h2. 3. Prerequisites
Before using this tool, ensure that the following prerequisites are met:

* Java 11 or higher installed
* Maven 3.8+ installed
* Sufficient memory and CPU resources

---

h2. 4. Project Structure
The project should be organized as follows to ensure smooth operation of the utility:
{code}
TIBCO-Migration-Utility/
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/example/tibcomigration/
│   └── test/
│       └── java/
│           └── com/example/tibcomigration/
├── src/main/resources/
│   ├── process/
│   │   └── <Tibco Process Files>
│   ├── xsd/
│   │   └── <XSD Files>
│   └── copybook/
│       └── <Copybook Files>
├── cb2xml.properties
├── pom.xml
├── README.md
└── LICENSE
{code}

*Note:* Ensure that the required files are placed in the appropriate directories before building the project.

h3. cb2xml.properties
Create a file named *cb2xml.properties* in the project root directory with the following configuration:
{code}
column.start=6
column.end=200
{code}
This file is used to define the parsing range for copybook files, ensuring accurate data extraction during the migration process.

---

h2. 5. POM Configuration
Provide a sample *pom.xml* file with necessary dependencies and plugins. You can adjust this section based on the specific requirements of the tool.

{code\:xml} <project xmlns="http://maven.apache.org/POM/4.0.0"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd"> <modelVersion>4.0.0</modelVersion> <groupId>com.example</groupId> <artifactId>tibco-migration-utility</artifactId> <version>1.0.0</version>

```
<dependencies>
    <!-- Core Dependencies -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter</artifactId>
        <version>3.0.0</version>
    </dependency>
    <dependency>
        <groupId>com.fasterxml.jackson.core</groupId>
        <artifactId>jackson-databind</artifactId>
        <version>2.15.0</version>
    </dependency>
    <dependency>
        <groupId>net.sf.cb2xml</groupId>
        <artifactId>cb2xml</artifactId>
        <version>1.5.0</version>
    </dependency>
</dependencies>

<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.11.0</version>
            <configuration>
                <source>11</source>
                <target>11</target>
            </configuration>
        </plugin>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```

</project>
{code}

---

h2. 6. Usage Guide
Provide a step-by-step guide on how to use the tool, including commands, configuration examples, and best practices.

---

h2. 7. Troubleshooting
Common issues and their solutions. Include links to logs or screenshots where necessary.

---

h2. 8. Contact and Support
Provide contact information for technical support or additional assistance.

---

h2. 9. Appendix
Include any additional information, resources, or references that may be helpful for users.
