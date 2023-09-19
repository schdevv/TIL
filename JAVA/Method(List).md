#### JAVA

### 1. Method (List)

#### 1) List
```java
List<String> List = new ArrayList<>();

list.add("서울") // list의 가장 뒤에 서울 값을 삽입
list.add(1, "대전") // 1의 위치에 대전 값을 삽입
list.addAll(list2) // list의 뒤에 list2의 모든 값을 삽입

list.get(0) // 0 위치의 값을 반환 (서울) 
list.set(0, "대구") // 0 위치의 값을 대구로 변경

list.indexOf(대구) // 대구의 첫번째 인덱스 값을 반환 = 0
list.lastIndexOf("대구") // 대구의 마지막 인덱스 값을 반환 = 0

list.remove(0) // 0 위치의 값을 삭제
list.remove("대구") // 첫번째 대구 삭제
list.removeAll(list2) // list에서 list2에 들어있는 모든 값을 삭제
list.retainAll(list2) // list에서 list2에 들어 있는 값을 제외하고 모든 값을 삭제

list.clear() // 모든 값을 삭제
list.isEmpty() // 길이가 0이면 true, 아니면 false
list.size() // 길이를 출력

list.contains("서울") // 서울이 list에 있으면 true, 아니면 false
list.containsAll(list2) // list에 list2의 모든 값이 포함되면 true, 아니면 false

list.removeIf(k -> k % 2 != 0) // 람다식으로 홀수를 list에서 모두 제거 
```

#### 2) List <-> Array 형변환
```java
// 문자열 배열을 list로 변환
String[] temp = "abcde";
List<String> list = new ArrayList<>(Arrays.asList(temp));

// list를 문자열 배열로 변환
List<String> list = new ArrayList<>();
String[] temp = list.toArray(new String[list.size()]);

// 정수 배열을 List로 변환
int[] temp = {1123, 1412, 23, 44, 512132};
List<Integer> list = new ArrayList<>(Arrays.asList(temp));

// List를 정수 배열로 변환
List<Integer> list = new ArrayList<>();
int[] temp = list.stream().mapToInt(i->i).toArray();
```
