#### JAVA

### 1. 자료구조(Data Structure)

|NO|NAME|Content|Characteristics|Implementation|
|---|---|---|---|---|
|1|**Array**|고정된 크기의 연속된 메모리 공간에 동일한 데이터 타입을 저장|인덱스 기반의 빠른 접근, 크기 변경이 어려움||
|2|**List**|순서를 유지하며 객체를 저장하는 집합|동적 크기, 중복데이터 허용|ArrayList, LinkedList 등|
|3|**Set**|중복을 허용하지 않는 객체의 집합|집합 연산(합집합, 교집합 등)|HashSet, LinkedHashSet, TreeSet 등|
|4|**Map**|키-값 쌍으로 데이터를 저장, 중복을 비허용|키를 통한 빠른 데이터 접근이 용이함|HashMap, LinkedHashMap, TreeMap 등|
|5|**Queue**|FIFO방식으로 데이터를 저장|데이터의 삭제 : 앞 데이터의 추가 : 뒤|LinkedList (큐 인터페이스 구현)|
|6|**Stack**|LIFO방식으로 데이터를 저장|데이터의 추가, 삭제 : 뒤|Java 기본 라이브러리(Stack), 인터페이스(Deque)-ArraryDeque 등|
|7|**Tree**|노드들이 서로 연결된 계층적 구조로 데이터를 저장|노드 : 하나의 부모와 여러 자식으로 구성/ 탐색, 삽입, 삭제 연산이 로그시간에 이루어짐.|TreeSet, TreeMap(이진 탐색 트리) 등|
