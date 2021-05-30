## Char
Character 클래스에 대한 초기화는 String 클래스의 초기화와는 다르다.

### 초기화
- Character는 String과는 달리 double quotes가 아니라 single quotes로 처리한다.
- Character의 빈 값에 대한 초기화는 꼭 빈 값을 넣어줘야한다.

```java
char emptyChar = ' '; // ''는 안됨!
```

### null값 처리
- String처럼 null값을 바로 적용해주면 안되고 유니코드로 처리해줘야한다.

```java
char nullChar = '\u0000'; // null은 안됨!
```

[Previous Page](./arrays) / [Next Page](./stringBuilder)