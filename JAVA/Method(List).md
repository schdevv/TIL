#### JAVA

### 1. Method (List)

#### 1) List
```java
List<String> List = new ArrayList<>();

list.add("서울") //
list.add(1, "대전") //
list.addAll(list2) //

list.get(0) // 
list.set(0, "대구") //

list.indexOf(대구) //
list.lastIndexOf("대구") //

list.remove(0) //
list.remove("대구") //
list.removeAll(list2) //
list.retainAll(list2) //

list.clear() //
list.isEmpty() //
list.size() //

list.contains("서울") //
list.containsAll(list2) //

list.removeIf(k -> k % 2 != 0) //
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
