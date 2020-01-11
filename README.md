# oauth2-with-spring-boot

[gitignore.io](https://gitignore.io): macos, intellij, java, gradle → [.gitignore](https://gitignore.io/api/java,macos,gradle,intellij)

## [Spring Initializr](https://start.spring.io/)

### Dependencies

- Developer Tools
  - Spring Boot DevTool: 편리한 개발 환경 구축. LiveReload.
  - Lombok: 자바 코드 간소화
- Web
  - Spring Web: RESTful MVC 웹. Tomcat 사용.
- Template Engines
  - Mustache: Logic-less 템플릿
- Security
  - OAuth2 Client


## Start

### LiveReload

1. IntelliJ:
    1. Preferences:
        - Compiler: Build project automatically
    2. Registry: Cmd + Shift + A
        - compiler.automake.allow.when.app.running: check
1. Chrome: LiveReload

### Security Login Disable

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.boot.autoconfigure.security.servlet.SecurityAutoConfiguration;

@SpringBootApplication(exclude = {SecurityAutoConfiguration.class})
public class DemoApplication {

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }

}
```

