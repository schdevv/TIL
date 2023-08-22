#### Back-End

### 1. Java

##### 1. Java의 특징
```
(1) 객체지향 프로그래밍(OOP)
(2) 자동 메모리 관리(Garbage Collection)
(3) 독립적인 운영체제(JVM)
(4) 멀티쓰레드
(5) 동적 로딩
(6) 네트워크와 분산처리
```
##### 2. Java Thread와 Process의 차이
```
```
##### 3. Solid 원칙
```
```
##### 4. Java의 자료구조(Data Structure)
```
(1) 배열(Array)
(2) 리스트(List)
(3) 셋(Set)
(4) 맵(Map)
(5) 큐(Queue)
(6) 스택(Stack)
(7) 트리(Tree)
```
##### 5. Java의 동작원리
```
(1) 소스코드 작성 및 컴파일 : Java 소스파일에 코드를 작성하고 Java Compiler(javac)를 통해 소스코드를 바이트코드로 변환하여 .Class파일로 저장
(2) 클래스 로더 : JVM 시작 시, 클래스 로더 컴포넌트는 .Class 파일을 메모리에 로드
(3) 바이트코드 실행 : JVM의 실행 엔진이 로드된 바이트코드를 해석하고 실행하면, JIT(Just-In-Time) 컴파일러를 통해 바이트코드를 기계어로 변환하고 해당 코드를 플랫폼에서 실행
(4) 런타임 데이터 영역 : 실행결과를 멀티스레드 영역에 따라 런타임 데이터 영역에 저장
 - 메소드 영역 : 클래스, 메소드, 변수 정보 등
 - 힙 영역 : 객체와 배열이 생성되는 영역
 - 스택 영역 : 메소드의 호출과 로컬 변수 등
 - PC 레지스터 : 현재 실행 중인 JVM 명령의 주소를 저장
 - 네이티브 메소드 스택 : 네이티브 메소드의 정보를 저장
(5) Garbage Collection : Garbage Collector를 통해 메모리를 자동으로 관리
 - 사용되지 않는 객체를 메모리에서 제거해 힙 영역의 메모리를 회수함.
 - JVM에 의해 GC의 실행 시점이 결정됨.
 - 수동제어 : System.gc() 메소드 사용.
```

#### 6. 자바개발환경
```
(1) JVM(Java Vitural Machine) : 자바 어플리케이션을 실행하기 위한 가상 컴퓨터
(2) JRE(Java Runtime Environment) = JVM + 클래스라이브러리(Java API) : 자바실행환경
(3) JDK(Java Development Kit) = JRE + 개발에 필요한 실행파일 (Javac.exe 등) : 자바개발도구
```

### 2. DB
1. RDBMS
```
```

### 3. WEB
##### 1. RESTful API 방식
```
``` 

### 4. Spring
##### 1. Spring의 특징
```
```
##### 2. Spring Boot의 장점
```
```
##### 3. Spring MVC 패턴
```
```
##### 4. Build Tool
```
(1) Maven
(2) Gradle
```

### 5. 배포
```
```

### 6. ORM
```
(1) JPA
```

### 7. Security
```
(1) Spring Security
(2) JWT
```

