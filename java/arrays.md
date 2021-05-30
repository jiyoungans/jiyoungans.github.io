## Arrays
오늘 기록할 API는  **Arrays** !!!<br>
Arrays class안에는 Array를 정렬하거나 Array안에 있는 요소를 찾는 등의 작업을 할 수 있는 여러 메소드가 있다.
이 메소드들은 모두 `NullPointerException`을 던진다.

### asList(arr)
- Array 안의 요소를 Array length만큼의 size를 가진 List에 넣어준 후, List를 return
- parameters
    - arr : list로 return할 array
- returns
    - array에서 return된 list

```java
int[] tempArr = new int[]{1,2,3,4,5};
List<Integer> tempList = Arrays.asList(tempArr); // tempList.get(0) == tempArr[0]... tempList.get(n) == tempArr[n]
```

### binarySearch(arr, fromIdx?, toIdx?, key)
- Array요소 중에 파라미터값인 key가 있는지 binary search algotirhm을 사용하여 검사
- 이 method를 사용하려면 array가 정렬되어 있어야한다. 그렇지 않으면, undefined가 return됨.
- parameters
    - arr : key를 찾을 array
    - fromIdx : 검색을 시작할 첫번째 index, binary search할 때, 해당 index를 포함한다. **(optional)**
    - toIdx : 검색을 시작할 마지막 index, binary search할 때, 해당 index를 제외한다. **(optional)**
    - key : 찾을 요소인 key
- returns
    - key가 array에서 위치하는 index

```java
int[] tempArr = new int[]{1,2,3,4,5};
int idx = Arrays.binarySearch(tempArr, 4); // idx = 3
```

### copyOf(arr, length)
- array를 특정 length를 새로운 array로 만들어준다.
- array를 copy해주되
    - 특정 length가 복사할 array보다 작으면 그 length까지만의 요소만 존재한다.
    - 특정 length가 복사할 array보다 크면 0이나 null로 나머지 index를 채운다.
- parameters
    - arr : 복사할 original array
    - length : original array를 복사해서 새로 만들 array의 length
- returns
    - original array를 특정 length만큼 복사해서 만든 array

```java
int[] tempArr = new int[]{1,2,3,4,5};
int[] smallNewArr = Arrays.copyOf(tempArr, 3); // smallNewArr = [1,2,3]
int[] bigNewArr = Arrays.copyOf(tempArr, 7); // bigNewArr = [1,2,3,4,5,6,7]
```

### copyOfRange(arr, from, to)
- array의 특정 위치에 있는 요소들을 가져와서 새로운 array로 만들어준다.
- parameters
    - arr : 복사할 original array
    - from : array에서 복사를 시작할 요소의 시작 index. 해당 index가 포함된다.
    - to : array에서 복사를 시작할 요소의 마지막 index. 해당 index는 제외된다.
- returns
    - original array의 특정 위치에 있는 요소들을 복사해서 만든 array

```java
int[] tempArr = new int[]{1,2,3,4,5};
int[] newArr = Arrays.copyOfRange(tempArr, 2, 4); // smallNewArr = [3,4]
```

### toString(arr)
- array안의 요소를 string 형태로 나타내준다. 예) "[1, 2, 3]" 이 형태로!
- parameters
    - arr : String으로 변환해서 나타낼 Array
- returns
    - String으로 변환된 array

```java
int[] tempArr = new int[]{1,2,3,4,5};
String arrToStr = Arrays.toString(tempArr); // [1, 2, 3, 4, 5] 가 출력된다.
```

[Previous Page](./map) / [Next Page](./char)