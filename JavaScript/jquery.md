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

+ 문서에 jQuery 라이브러리를 불러오지 않고 $( ) 함수를 사용하려고 하면 ReferenceError가 발생한다.

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

+ <b>html( )</b> : HTML 태그가 포함된 내용을 읽거나 설정함.

<br>   
<br>  

```javascript
// 텍스트 가져오기
console.log($('#content').text());

// 텍스트 설정하기
$('#content').text('Hello, World');
```

<br>   

+ <b>text( )</b> : HTML 태그가 제외된 텍스트를 읽거나 설정함.

<br>   
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

+ <b>val( )</b> : 폼 요소의 값(value)을 읽거나 설정함. 

<br>   
<br>   
<br>   
<br>   
<br>   

## jQuery 조작 (2)

<br>   

```javascript
// 속성 값 가져오기
console.log($("a").attr('href'));

// 속성 하나만 설정하기
$('a').attr('href', 'https://www.naver.com');

// 속성 여러개 설정하기
$('a').attr({
    'src': '/images/flower.jpg',
    'alt': 'A beautiful flower',
    'width': '500px'
});

// 속성 제거하기
$('img').removeAttr('alt');
```

<br>   

+ <b>attr( )</b> : 해당 요소의 속성을 읽거나 설정함.

<br>
<br>

```javascript
// 스타일 속성 값 가져오기
console.log($('#div1').css('background-color')); 

// 스타일 속성 하나만 설정하기
$('#Div1').css('background-color', 'blue');

// 스타일 속성 여러개 설정하기
$('#div1').css({
    'background-color': 'green',
    'color': 'hotpink',
    'font-size': '20px'
});
```

<br>   

+ <b>css( )</b> : 해당 요소의 스타일 속성을 읽거나 설정함.

<br>   
<br>   

```javascript
// 클래스 추가하기
$('#div1').addClass('highlight');

// 클래스 제거하기
$('#div1').removeClass('highlight');

// 클래스 토글하기 (없으면 추가, 있으면 제거)
$('#div1').toggleClass('highlight');

```

<br>   

+ <b>addClass( )</b> : 해당 요소에 하나 이상의 클래스를 추가함.
+ <b>removeClass( )</b> : 해당 요소에서 하나 이상의 클래스를 제거함.

<br>   
<br>   
<br>   
<br>   
<br>   

## jQuery 조작 (3)

<br>   

```javascript
let links = [
    {name: '네이버', url: 'https://www.naver.com'},
    {name: '구글', url: 'https://www.google.co.kr'},
    {name: '페이스북', url: 'https://www.facebook.com'}
]

$.each(links, (index, item) => {
    $('body').append(`<p><a href="${item.url}">${item.name}</a></p>`);
});
```

<br>   

+ vanilla JS의 <b>forEach( )</b> 콜백함수에서는 첫 번째 인자가 요소이며, 두 번째 인자가 인덱스다.
+ 반면 jQuery의 <b>each( )</b> 콜백함수에서는 첫 번째 인자가 인덱스이고, 두 번째 인자가 요소다.

<br>
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
