#### Back-End

### 1. Java

##### 1. Java의 특징
```
(1) 객체지향 프로그래밍(Object-Oriented Programming) : 코드의 재사용, 유지보수, 중복제거, 오작동 방지(클래스, 객체, 캡슐화, 다형성, 추상화)
(2) 자동 메모리 관리(Garbage Collection) : Garbage Collector를 통한 메모리 관리
(3) 독립적인 운영체제(JVM) : 자바 프로그램은 JVM을 통해 동작하기 때문에, 운영체제에 독립적임. 단, JVM이 운영체제에 종속적임.
(4) 멀티쓰레드(Multi Tread) : 다양한 쓰레드 영역을 시스템에 관게 없이 JAVA API를 활용해 구현이 가능함.
(5) 동적 로딩(Dynamic Loading) : 자바 프로그램 실행 시, 모든 클래스를 수행하지 않고 필요한 시점에서 클래스를 로딩함. 적은 자원으로 변경사항에 따른 유지보수 가능.
(6) 네트워크와 분산처리 : Java API를 사용해 인터넷의 방대한 분산처리 가능.
```
##### 2. Java Thread와 Process의 차이
```
(1) Process : JVM이 시작될 때 생성되며, JVM이 종료될 때 까지 계속 존재함(JVM 자체)
(2) Thread : JVM 내에서 실행되는 개별적인 실행 흐름(병렬로 실행되는 각각의 작업 단위)
```

##### 3. Solid 원칙
```
(1) S (Single Responsibility) : 단일책임의 원칙, 하나의 클래스는 하나의 책임을 가진다.
(2) O (Open/Closed) : 클래스는 확장은 열려있고 수정은 닫혀야한다. 기존 코드를 변경하지 않고 기능을 수정해야 한다.
(3) L (Liskov Substitution) : 상속과 다형성, 하위 클래스는 상위 클래스의 인스턴스를 대체할 수 있어야 함.
(4) I (Interface Segregation) : 클래스가 필요로하는 구체적이고 작은 여러가지 인터페이스로 세분화하는 것이 바람직함. 
(5) D (Dependency Inversion) : 유연성과 확장성을 위해서 구체적인 구현보다 인터페이스나 추상 클래스에 의존해야 함.
```
##### 4. Java의 자료구조(Data Structure)
```
(1) 배열(Array) : 고정된 크기의 연속된 메모리 공간에 동일한 데이터 타입을 저장
 - 인덱스 기반의 빠른 접근
 - 크기 변경이 어려움
(2) 리스트(List) : 순서를 유지하며 객체를 저장하는 집합
 - 동적 크기
 - 중복데이터 허용
 - 구현체 : ArrayList, LinkedList 등
(3) 셋(Set) : 중복을 허용하지 않는 객체의 집합
 - 집합 연산(합집합, 교집합 등)
 - 구현체 : HashSet, LinkedHashSet, TreeSet 등
(4) 맵(Map) : 키-값 쌍으로 데이터를 저장, 중복을 비허용
 - 키를 통한 빠른 데이터 접근이 용이함.
 - 구현체 : HashMap, LinkedHashMap, TreeMap 등
(5) 큐(Queue) : FIFO방식으로 데이터를 저장
 - 데이터의 삭제 : 앞
 - 데이터의 추가 : 뒤
 - 구현체 : LinkedList (큐 인터페이스 구현), PriorityQueue 등
(6) 스택(Stack) : LIFO방식으로 데이터를 저장
 - 데이터의 추가, 삭제 : 뒤
 - 구현체 : Java 기본 라이브러리(Stack), 인터페이스(Deque)-ArraryDeque 등
(7) 트리(Tree) : 노드들이 서로 연결된 계층적 구조로 데이터를 저장
 - 노드 : 하나의 부모와 여러 자식
 - 탐색, 삽입, 삭제 연산이 로그시간에 이루어짐.
 - 구현체: TreeSet, TreeMap(이진 탐색 트리) 등
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

### 2. Database
1. RDBMS(Relational Database Management System)
- 관계형 데이터베이스 관리 시스템
```
(1) 테이블 구조 : 행(row)과 열(column) 구성
(2) 데이터 무결성 : 제약 조건(Constraints) 설정
(3) SQl 사용
(4) 데이터 동시성 : 여러 사용자가 동시에 DB로 엑세스 할 경우, 데이터의 일관성 및 무결성을 보장함
(5) 데이터베이스 정규화 : 데이터 중복 최소화 및 무결성 유지가 목적, DB설계 과정에서 작업 수행
(6) 트랜잭션 관리 : 데이터 베이스 작업들이 모두 수행되거나 반대로 수행되지 않도록 관리해 일관성을 유지함
(7) 백업 및 복구 : 데이터 손실 및 장애 상황에서 데이터 복구 가능
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

