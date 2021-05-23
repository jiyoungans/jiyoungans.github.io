## Map 에서 key 값 null 처리
Map에서 key값이 null 인 경우를 처리할 때, 항상 if문을 통해서 처리했었다.
하지만 java 8 에서부터는 method로 간편하게 처리할 수 있는 방법이 있다!

### Map.getOrDefault(key, defaultValue)

- key가 없을 때, null이 아니라 설정해 놓은 defaultValue로 값이 return 된다.
- null처리를 따로 해주지 않아도 되기 때문에 라인수도 짧아지고, 가독성이 높아진다.

#### AS-IS
```java
for(String comp: completion) {
    int value = 1;

    if(nameMap.get(comp) != null) {
        value = nameMap.get(comp) + 1;
    }

    nameMap.put(comp, value);
}
```

#### TO-BE
```java
for(String comp: completion) {
    nameMap.put(comp, nameMap.getOrDefault(comp, 0) + 1);
}
```

[Previous Page](./random)
<!-- / [Next Page](./another-page.html) -->