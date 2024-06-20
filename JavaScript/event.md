## 클릭 이벤트

<br>   

```html
<div>
    <h3>삭제 대상</h3>
    <input type="button" onclick="delEl()" style="color: red;" value="삭제">
</div>
```

<br>   

```javascript
function delEl() {
    const div = document.querySelector("div");
    const h3 = document.querySelector("div > h3");
    div.removeChild(h3);
}
```

<br>   
<br>   
<br>   
<br>   
<br>   

## 키보드 이벤트

<br>   

```html
<h1><span id="cnt">0</span>/ 100</h1>
<textarea cols="20" rows="10"></textarea>
```

<br>  

```javascript
document.addEventListener('DOMContentLoaded', () => {
    const textarea = document.querySelector('textarea');

    textarea.addEventListener('keyup', (event) => {
        const str_len = event.currentTarget.value.length;
        const cnt = document.getElementById("cnt");
        cnt.innerText = str_len;
        if(str_len > 100) {
            alert('100글자까지 작성이 가능합니다.');
        }
    })
})
```

<br>   
<br>   
<br>   
<br>   
<br>   

## 선택지 이벤트

<br>   

```html
<h2 class="print"></h2>

<select>
    <option>HTML</option>
    <option>CSS</option>
    <option>JavaScript</option>
    <option>JQuery</option>
    <option>React</option>
</select>
```

<br>   

```javascript
document.addEventListener('DOMContentLoaded', () => {
    const select = document.querySelector("select");
    const h2_print = document.querySelector("h2.print");

    select.addEventListener("change", (event) => {
        const options = event.currentTarget.options;
        const index = event.currentTarget.options.selectedIndex;
        h2_print.textContent = `선택 항목 : ${options[index]}`
    })
})
```

<br>   
<br>   
<br>   
<br>   
<br>   

## 라디오 이벤트

<br>   

```html
<h3>관심 있는 언어를 선택하세요!</h3>

<input type="radio" name="lang" value="JAVA" id="JAVA" checked>
<label for="JAVA">JAVA</label>

<input type="radio" name="lang" value="PYTHON" id="PYTHON">
<label for="PYTHON">PYTHON</label>

<input type="radio" name="lang" value="C++" id="C++">
<label for="C++">C++</label>

<h3 id="output">선택 언어 : JAVA</h3>
```

<br>   

```javascript
document.addEventListener('DOMContentLoaded', () => {
    const h3_output = document.querySelector("h3#output");
    const radios = document.querySelectorAll('[name=lang]');
    
    radios.forEach((radio) => {
        radio.addEventListener("change", (event) => {
            const currentRadio = event.currentTarget;
            if(currentRadio.checked) {
                h3_output.textContent = `선택 언어 : ${currentRadio.value}`;
            }
        })
    })
})
```
