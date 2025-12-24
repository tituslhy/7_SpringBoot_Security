# 7_SpringBoot_Security
Using SpringBoot's default security frameworks

Simply add this to your pom.xml file:
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```
and Springboot will automatically generate security for your endpoints. 
We will be required to submit login credentials when accessing your APIs. 

When starting your application, look for a line in the stdout stating:
```text
Using generated security password: ....
```

Note that the default username is "user".

## To override the login credentials
Edit the application.properties file with:
```yaml
spring.security.user.name=...
spring.security.user.password=...
```

Alternatively, create an annotated `@Configuration` class with an InMemoryManager instance and SpringBoot will use credentials from here instead.

The main class is `DemoSecurityConfig.java`