#### JAVA

### 1. Method(StringBuilder)

#### 1) StringBuilder
```java
// String은 한번 만들어지면 문자를 추가하거나 삭제 할 수 없는 변경이 불가능한 구조.
// StringBuilder는 문자열의 변경이 가능한 구조.

StringBuilder sb = new StringBuilder();  

sb.append("abc") // 문자열 추가
sb.insert(2, "kk") // 2 위치에 kk 값을 삽입 : abkkc

sb.delete(0, 2) // 0~1 위치의 문자열을 삭제 : kkc
sb.deleteCarAt(2) // 2 위치의 문자를 삭제 : kk

sb.setCharAt(0, 'h') // 0 위치의 문자를 h로 변경 : hk

sb.reverse() // 문자열을 역순으로 정렬 : kh

sb.setLength(2) // 문자열의 길이를 2로 줄임 : kh
sb.setLength(4) // 문자열의 길이를 4로 늘림 : kh null null (늘어난 부분은 null 문자로 채워짐)
```
