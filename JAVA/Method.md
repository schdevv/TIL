#### JAVA

### 1. 자바의 Method 정리

#### 1) Queue
```java
Queue<Integer> queue = new LinkedLIst<>();

queue.add(1) // 값 추가
queue.ofter(2) // 값 추가
queue.poll() // 첫 번째 값 반환, 비어있으면 null 반환
queue.remove() // 첫 번째 값 제거
queue.clear() // 모든 값 삭제
queue.peek() // 첫 번쨰 값 출력 (제거 X)
```

#### 2) Priority Queue
```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
//기본적으로 낮은 숫자가 우선순위를 갖는다.
// 높은 숫자가 우선되게 하려면 () 안에 Collections.reverseOrder()를 작성한다.

pq.add(1) // 값 추가
pq.ofter(1) // 값 추가
pq.poll() // 첫 번째 값 반환, 비어있으면 null 반환
pq.remove() // 첫 번째 값 제거
pq.clear() // 모든 값 제거
pq.peek() // 첫 번째 값 출력
```

#### 3) HashSet
```java
HashSet<Integer> set = new HashSet<>();
// HashSet : 중복을 허용하지 않는 자료구조, 순서가 없고 정렬도 없음.
// LinkedHashSet : 중복을 허용하지 않는 자료구조, 삽입된 순서대로 배열을 관리함
// TreeSet : 중복을 허용하지 않는 자료구조, 이진탐색트리 형태로 정렬해 데이터를 저장함

set.add(1) // 값 추가
set.remove(1) // 값이 1인 데이터를 삭제함
set.removeAll(set2) // set의 데이터 중 set2에 들어있는 모든 데이터를 삭제
set.retainAll(set2) // set의 데이터 중 set2에 들어있지 않은 데이터를 모두 삭제
set.clear() // 모든 데이터 삭제
set.size() // 크기를 반환
set.contains(1) // 값이 1이면 true, 없으면 false

// HashSet의 값을 출력하는 방법
// 1) Iterator(이터레이터) : get 메소드 없이 원소에 접근하는 방법
Iterator iter = set.iterator();
while (iter.hashNext())
    System.out.print(iter.next());

// 2) 
```