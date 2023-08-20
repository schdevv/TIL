#### Spring Boot

### Springfox (Library)
- Swagger를 갈편하게 통합하는 기능을 제공
1. 적용방법

(1) Maven 의존성 추가
```java
<dependency>
    <groupId>io.springfox</groupId>
    <artifactId>springfox-boot-starter</artifactId>
    <version>3.0.0</version>
</dependency>
```
(2) Java 설정
```java
@Configuration
@EnableSwagger2
public class SwaggerConfig {
    @Bean
    public Docket api() {
        return new Docket(DocumentationType.SWAGGER_2)
                .select()
                .apis(RequestHandlerSelectors.basePackage("com.yourpackage"))
                .paths(PathSelectors.any())
                .build();
    }
}
```
(3) Swagger UI 적용확인
```
Spring Boot 애플리케이션 실행 후 웹브라우저 접속 : http://localhost:8080/swagger-ui.html
```
