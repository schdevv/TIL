#### JAVA

### 1. Method(Collections)

#### 1) Collections
```java
int[] arr = { 1123, 1412, 23, 44, 512132 };

List<Integer> list = new ArrayList<>(Arrays.asList(arr)); //배열을 리스트로 변환

Collections.max(list) // list의 원소 중 가장 큰 값을 반환 
Collections.min(list) // list의 원소 중 가장 작은 값을 반환

Collections.sort(list) // list를 오름차순으로 정렬
Collections.sort(list, Collections.reverseOrder()) // list를 내림차순으로 정렬

Collections.reverse(list) // list의 순서를 역순으로 정렬

Collections.frequency(list, 23) // list 내의 23의 개수를 반환

Collections.binarySearch(list, 44) // 최초로 검색된 44의 인덱스 1을 반환
// 44의 값이 없다면, 보다 큰 최초의 수 위치 2를 찾아서 -1을 곱하고 1을 빼서 반환 (-3)
```
