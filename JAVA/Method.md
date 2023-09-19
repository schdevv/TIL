#### JAVA

### 1. 자바의 Method 정리

#### 1) String
```java
String str = "abcde"; // 초기화

str.length() // str의 길이를 반환
str.isEmpty() // str의 길이가 0이면 true, 아니면 false

str.charAt(2) // 인덱스로 str의 문자를 찾음 = "c" 반환
str.indexOf("c") // 문자로 첫번째 인덱스 찾기 = 값 2 반환
str.lastIndexOf("c") // 문자의 마지막 인덱스 찾기 = 값 2 반환

str.substring(2, 4) // 2~3번째 위치의 문자열을 반환(시작~전 까지) = "cd" 
str.substring(3) // 3부터 끝까지의 문자열 반환 = "de"

str.replace('b', 'k') // b를 k로 변경 = akcde

str.equals("abcde") // str과 값을 비교해서 같으면 true, 다르면 false 
str.contains("bc") // str에 bc가 포함되어 있으면 true, 아니면 false

str.split(" ") // 띄어쓰기로 구분된 문자열 str을 분리해서 String[] 배열로 반환 
// 개별 값 출력 예시
Stirng str1 = "Hello World"
String[] result = str.split(" ");
    System.out.println(result[0]); // "Hello"
    System.out.println(result[1]); // "World"

// 모든 원소 일괄 출력 예시(Arrays)
import java.util.Arrays;
str.split() // 띄어쓰기 없는 문자를 str을 한 문자씩 분리해서 String[] 배열로 반환

str.trim() // 

str.toLowerCase() // 
str.toUpperCase() //

str.compareTo("abcdd") //

Integer.parseInt("300") // 
Integer.toString(300) // 
```
