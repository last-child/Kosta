## 01. css( ) 함수

<br>   

```javascript
// Vanilla

// 페이지의 모든 콘텐츠가 로드되고 난 후 실행함
document.addEventListener("DOMContentLoaded", () => {

    // h2 요소의 스타일 속성을 지정함.
    document.querySelectorAll('h2').forEach((item) => {
        item.style.fontSize = '40px';
    })

    // h3 요소의 스타일 속성들을 한 번에 지정함.
    document.querySelectorAll('h3').forEach((item) => {
        item.style.color = 'red';
        item.style.backgroundColor = "yellow";
    })

})
```

```javascript
// JQuery

$(document).ready(() => {
    $('h2').css('font-size', '40px');
   
    $('h3').css({
        'color': 'red',
        'background-color': 'yellow'
    });
})
```

#### jQuery의 css( ) 함수는 특정 요소의 스타일 속성을 가져오거나 설정할 수 있다.

<br>   
<br>   
<br>
<br>   
<br>

## 02. val( ) 함수

<br>   

```javascript
// Vanilla

document.addEventListener("DOMContentLoaded", () => {

    // 타입이 text인 input의 value를 지정함
    document.querySelector("input[type=text]").value = "안녕하세요";

    // 체크된 체크박스의 값을 가져옴
    const checkedBox = document.querySelector('input[type="checkbox"]:checked');
    const checked_val = checkedBox? checkedBox.value : null;
    console.log(checked_val);

})
```

<br>   

```javascript
// JQuery

$(document).ready(() => {
    $("input:text").val("안녕하세요");

    const checked_val = $('input:checkbox:checked').val();
    console.log(checked_val);
})
```

#### jQuery의 val( ) 함수는 특정 폼의 값을 가져오거나 설정할 수 있다.

<br>   
<Br>   
<br>   
<Br>   
<br>   

## 
