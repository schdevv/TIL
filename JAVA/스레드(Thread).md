#### JAVA

### 1. 스레드(Thread)

#### 1. 개념
- 프로세스 내에서 실행되는 특정한 실행 경로(실행흐름 모델).
- 같은 프로세스 내의 다른 스레드와 메모리, 자원을 공유함.
- 프로세스에 비해 상대적으로 자원 소모가 적음.  

#### 2. 구현체
- `java.lang.Thread` : 스레드 생성 및 관리
- `java.util.concurrent` : Executor Framework를 사용해 스레드 풀, 콜러블, 퓨처 다양한 API로 보다 효율적인 스레드 관리

#### 3. 생성 및 실행
- `Thread` 클래스를 상속받아 `run()` 메서드를 오버라이드 하는 방법
- `Runnable` 인터페이스를 구현하는 객체를 생성하고, 이를 Thread 객체의 파라미터로 전달하는 방법

```java
Thread thread = new Thread(new Runnable() {
    @Override
    public void run(){
        //실행코드
    }
});
thread.start();
```
- 수행과정
```
(1) start() 메서드에 의해 시작되고 스케쥴러를 통해 run() 메서드 실행.
(2) 이후 스레드 사용은 run() 메서드를 오버라이드하여 구현할 수 있음.
(3) 스레드의 시작은 start() 메서드를 통해서만 수행되어야 함.
```

#### 4. 생명주기

|NO|NAME|Content|
|---|---|---|
|1|**New(생성)**|Thread 생성, start() 메서드는 호출되지 않은 상태|
|2|**Runnable(실행 가능)**|start()메서드를 호출한 상태 : Thread 실행이 가능한 상태(Ready: CPU 점유율 0%)|
|3|**Waiting(대기)**|Thread가 다른 Thread의 특정 작업을 기다리는 상태(ex. join() 메서드 사용)|
|4|**Timed Waiting**|특정 시간동안 대기하는 상태(ex. sleep() 메서드 사용)|
|5|**Blocked(차단)**|Thread가 사용하려는 리소스에 대한 동기화가 된 블록에 접근할 경우, 다른 Thread에 의해 차단된 상태(지연 상태 : CPU점유권 상실)|
|6|**Terminated(종료)**|Thread의 작업이 종료되거나 비정상적으로 종료된 상태|

#### 5. 우선권
- Thread는 `우선순위(Priority)`를 가지며, 이를 기반으로 스케줄링이 가능함.
(1) `Thread.MIN_PRIORITY`(1)부터 `Thread.MAX_PRIORITY`(10)까지의 범위로 우선순위 지정
(2) 기본 우선순위 : `Thread.NORM_PRIORITY`(5)
(3) `setPriority(int new Priority)` 메서드를 사용해 우선순위를 설정할 수 있음.


### 2. 멀티스레드(Multi Thread)

#### 1. 개념
- 한 프로세스 내에서 여러 Thread가 동시에 실행되는 상태
- CPU의 사용률과 자원을 효율적으로 활용할 수 있음.

#### 2. 동시성 문제
- `경쟁 조건 (Race Condition)` : 두 개 이상의 스레드가 공유 데이터를 동시에 로딩할 경우, 스레드의 실행순서나 타이밍에 따라 결과가 달리지거나 오류발생.
- `교착 상태 (Deadlock)` : 두 개 이상의 스레드가 서로 다른 자원(메모리, 파일, 세마포어 등)을 보유했지만, 서로에게 없는 자원을 기다리는 경우, 해당 자원을 얻을 수 없기에 작업 수행이 멈추는 상태(무한대기)
- `기아 상태 (Starvation)` : 일부 스레드가 다른 스레드보다 우선권이 낮거나 다른 원인으로 계속해서 실행이 되지 못하는 상태. 
- `라이브락 (Livelock)` : 두 개이상의 스레드가 서로간의 작업을 기다리면서 게속하여 작업을 시도하지만, 진행되지 못하는 상태(우선순위를 서로 미루는 상황)

#### 3. 동시성 문제 해결방법
- `락 (Lock)`: 자원에 접근할 때 락을 사용하여 한 번에 하나의 스레드만 접근하도록 제한.
- `세마포어 (Semaphore)`: 한 번에 여러 스레드가 자원에 접근할 수 있도록 제한하는 카운터 기반의 동기화 메커니즘.
- `모니터 (Monitor)`: 락과 조건 변수를 결합한 고급 동기화 방법으로, 특정 조건 하에서만 자원에 접근하도록 제한.