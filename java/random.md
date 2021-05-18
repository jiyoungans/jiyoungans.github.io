## Math.Random()  vs  Random Class
두 가지 방법 모두 난수를 획득한다는 점은 동일하다.

### Math.Random()

- 시드값으로 현재 시간을 사용하기 때문에 호출할 때마다 매번 다른 숫자가 획득된다.
- 0.0 ~ 1.0 사이의 무작위 실수가 획득
- 원하는 자리수만큼 곱한다음, int형으로 변환해주면 정수로 사용이 가능하다.

```java
int num = (int) ((Math.Random() * 100) + 1); // 1 ~ 100 사이의 난수
```

### Random Class

- 객체 생성을 통해 난수를 획득한다.
- 무작위 정수, boolean, float, long 값을 메소드를 통해 각각 획득할 수 있다.
- seed : 난수 알고리즘이 처음 시작되는 지점(숫자)를 말한다. 따라서, seed가 같은 Random객체들은 같은 순서대로 난수를 리턴한다.
- 주요 Methods
  
|Method명|설명|
|-------|---|
|nextInt()|무작위 정수 획득|
|nextInt(n)|0~n까지의 무작위 정수 획득|
|nextBoolean()|무작위 boolean획득|
|nextFloat()|무작위 float 획득|
|nextLong()|무작위 long 획득|
|setSeed(n)|난수를 발생시키는 초기숫자인 seed를 설정하는 메소드|
  
```java
Random test = new Random();
test.setSeed(10);
for(int i = 0; i < 2; i++) {
    for(int j = 0; j < 5; j++) {
        test.nextInt(10); // 0 ~ 10까지의 난수가 5번 반복되며, 같은 순서로 2세트가 출력됨
    }
}
```

[Previous Page](./shallowcopy)
<!-- / [Next Page](./another-page.html) -->