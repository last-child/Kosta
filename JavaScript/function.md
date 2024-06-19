## 콜백 함수 (1)

<br>   

#### JS의 함수는 1급 객체이기 때문에 변수에 저장될 수 있고, 다른 함수의 인수로 전달될 수 있다.
#### 다른 함수의 인수로 전달되는 함수를 콜백 함수라 한다.

<br>   
<br>   

```javascript
// 콜백 함수 정의
function printMessage(message) {
    console.log(message);
}

// 콜백 함수를 인자로 받는 함수 정의
function executeCallback(callback) {
    callback('Hello, World!');
}

// 함수 호출
executeCallback(printMessage);
```

<br>   

#### executeCallback 함수를 호출할 때 printMessage 함수의 레퍼런스를 인수(콜백 함수)로 전달한다.
#### executeCallback 함수가 실행될 때 특정 문자열이 printMessage 함수에 인수로 전달된다.
#### printMessage 함수가 실행되어 해당 문자열이 출력된다.

<br>   
<br>   
<br>   
<br>   
<br>   

## 콜백 함수 (2)

<br>   

#### 배열의 반복 메서드는 전달받은 콜백 함수를 배열의 요소별로 한 번씩 실행한다.
#### 콜백 함수가 실행될 때마다 value, index, array 순으로 인자들이 전달된다.

<br>   

+ value: 현재 처리 중인 요소의 값
+ index: 현재 처리 중인 요소의 인덱스
+ array: 현재 처리 중인 배열의 레퍼런스

<br>   
<br>   

```javascript
const array = [2, 3, 5, 7, 11];

const callBack = function(val, index) {
    console.log(index, val);
}

array.forEach(callBack);
```

<br>   

#### forEach 메서드는 배열의 요소별로 콜백 함수를 한 번씩 실행한다.
#### 예제에서는 forEach 메서드를 통해 인덱스와 요소를 출력하였다.

<br>  
<br>  

```javascript
const array = [2, 3, 5, 7, 11];

const square = function(x) {
  return x * x;
}

console.log(array.map(square));
```

<br>   

#### map 메서드는 요소마다 callBack 함수를 실행하되, 결과값들을 모아 새로운 배열로 반환한다.
#### 예제에서는 map 메서드를 통해 각 요소들을 제곱하여 새로운 배열을 생성하였다.

<br>   
<br>   

```javascript
const array = [2, 3, 5, 7, 11];

const callBack = function(y) {
  return y % 3 == 2;
}

console.log(array.filter(callBack));
```

<br>   

#### filter 메서드는 콜백 함수의 실행 결과가 true인 요소들만 모아 새로운 배열로 반환한다.
#### 예제에서는 filter 메서드를 통해 3으로 나눈 나머지가 2인 요소만을 필터링하였다.
