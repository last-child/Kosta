## jQuery 사용

<br>   

```javascript
// Vanilla

// 페이지의 모든 콘텐츠가 로드되고 난 후 실행함
document.addEventListener("DOMContentLoaded", () => {
    document.querySelectorAll('h1').style.color = 'red';
})
```

<br>   

```javascript
// jQuery (1)

$(document).ready(() => {
    $('h1').css('color', 'blue');
})
```

<br>   

```javascript
// jQuery (2)

$(() => {
    $('h1').css('color', 'blue');
})
```

<br>   

#### 문서에 jQuery 라이브러리를 불러오지 않고 $( ) 함수를 사용하려고 하면 ReferenceError가 발생한다.

<br>   
<br>   
<br>
<br>   
<br>

## jQuery 조작 (1)

<br>   

```javascript
// HTML 요소 가져오기
console.log($('#content').html());

// HTML 요소 설정하기
$('#content').html('<p>Hello, World</p>');
```

<br>   

```javascript
// 텍스트 가져오기
console.log($('#content').text());

// 텍스트 설정하기
$('#content').text('Hello, World');
```

<br>   

```javascript
// 입력 필드의 값 가져오기
const selected_val = $('select>option:selected').val();
console.log('selected_val :', selected_val);

const checked_val = $('input:checkbox:checked').val();
console.log(checked_val);

// 입력 필드의 값 설정하기
$('input:text').val('문자를 입력하세요.');
```
<br>   

#### html( ) : HTML 태그가 포함된 내용을 가져오거나 설정함.
#### text( ) : HTML 태그가 제외한 텍스트를 가져오거나 설정함.
#### val( ) : 폼 요소의 값(value)을 가져오거나 설정함. 

<br>   
<Br>   
<br>   
<Br>   
<br>   

## 요소를 필터링하는 함수

<br>   

```javascript
$('h3').filter((index, item) => {
    console.log(index, item)
    return index%3 == 0
}).css('color', 'blue')
```

<br>   

```javascript
$('table tr').filter(":even").css('color', 'blue');
$('h2').filter(":odd").css("color", "white");
```
