#### JPA (Java Persistence API)

### 1. ORM이란?
- DB의 Table과 프로그래밍 언어의 객체를 매핑하는 프로그래밍 기법.
- 객체지향 프로그래밍에서 DB를 효율적이고 간결하게 처리할 수 있음.
```
```

### 2. JPA
- Java에서 제공하는 ORM 표준 명세.
- 인터페이스의 집합으로 제공됨.
- 사용을 위해 구현체가 필요함.

|NO|NAME|Content|
|---|---|---|
|1|**EntityManager**|데이터베이스의 CRUD 작업을 처리하는 기본 인터페이스|
|2|**Entity**|JPA를 사용하여 데이터베이스 테이블과 매핑되는 Java 객체|
|3|**JPQL (Java Persistence Query Language)**|엔터티 객체를 조회하기 위한 쿼리 언어|

### 3. Hibernate
- JPA의 대표적인 구현체
- DB와 독립적인 작동
- 다양한 DB 시스템 간의 이동이 간편함
- 성능 최적화, 다양한 쿼리 옵션 추가 기능

### 4. Swagger
- API 개발을 위한 프레임워크
- API 명세(specification)
- 문서화(Documentation)

|NO|NAME|Content|
|---|---|---|
|1|**Swagger UI**|웹 기반 인터페이스로, 사용자는 API를 시각화, 테스트, API 문서화 제공|
|2|**Swagger Editor**|Swagger API 명세를 작성하고 편집하는 도구|
|3|**Swagger Codegen**|Swagger 명세를 기반으로 서버 스텁 및 클라이언트 SDK 생성을 지원하는 도구|