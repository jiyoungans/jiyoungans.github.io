## Shallow Copy  vs  Deep Copy

### Shallow Copy

원본 객체의 메모리주소를 참조하여 복사하는 방식 (참조 공유)  
복사한 객체에서 값이 변경되면, 원본 객체의 값도 같이 변경된다.

```java
int originArr[] = {2,3,4};
int copyArr[] = originArr;
copyArr[2] = 5; // originArr[2] 도 5로 변경된다.
```

### Deep Copy

원본 객체와 참조를 공유하지 않고, 새로운 주소에 담아 아예 새로운 객체로 만들어 복사하는 방식

```java
int originArr[] = {2,3,4};
int copyArr[] = originArr.clone();
copyArr[2] = 5; // originArr[2]는 그대로 4이다.
```

[Next Page](./random)