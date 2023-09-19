#### JAVA

### 1. Method(Data Structure)

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
    System.out.println(iter.next());

// 2) for-each문 
for (String item: set)
    System.out.println(item);
```

#### 4) HashMap
```java
// HashMap : <key, value> 쌍으로 특정한 규칙이 없이 저장되는 자료구조
// LinkedHashMap : key값의 입력순으로 정렬되며 <key, value> 쌍으로 저장되는 구조
// TreeMap : Key값이 알파벳순(오름차순)으로 정렬되며 <key, value> 쌍으로 저장되는 구조

HashMap<Integer, String> map = new HashMap<>();
HashMap<String, String> map = new HashMap();

map.put(1, "사과")
map.put(2, "바나나")
map.put(1, "포도") // key1의 value값이 후순위인 "포도"로 대체 됨. (Hash자료구조는 중복이 없음.)

map.remove(1) // key 값으로만 요소를 삭제함
map.clear() // 모든 데이터 삭제
map.containskey(1) // key의 값 중 1의 값이 있으면 true, 없으면 false
map.containsValue("사과") // value 중 "사과"가 있으면 true, 없으면 false

// HashMap의 값을 출력하는 방법
// 1) 하나의 key와 value를 출력
for (Integer i : map.keySet())
    System.out.println(i + map.get(i)); // i의 값이 1일 경우, 1과 "포도" 출력.
// 2) 모든 key와 value를 출력 
for (Entry<Integer, String> entry : map.entrySet())
    System.out.println(entry.getKey() + entry.getValue()); 
```