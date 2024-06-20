## 동적으로 요소 추가하기 (1)

<br>   

```javascript
document.addEventListener("DOMContentLoaded", () => {
    // wrap 요소 선택
    const wrap = document.querySelector("#wrap");

    // 새로운 h2 요소 생성 및 스타일 지정
    const h2_el = document.createElement('h2');
    h2_el.textContent = '동적으로 생성한 H2 tag';
    h2_el.style.textAlign = 'center';
    h2_el.style.color = 'blue';
    h2_el.style.backgroundColor = 'yellow';

    // 새로운 h2 요소를 wrap 요소에 추가
    wrap.appendChild(h2_el);

    // 새로운 img 요소 생성 및 경로 설정
    const img_el = document.createElement('img');
    img_el.setAttribute('src', '/images/teyvat.webp');

    // 새로운 img 요소를 wrap 요소에 추가
    wrap.appendChild(img_el);
})
```

<br>   

#### document.createElement(tag) 함수는 새로운 HTML 요소를 생성한다.
#### parent.appendChild(child) 함수는 새로운 요소를 하위 요소로 추가한다. 

<br>   
<br>   
<br>   
<br>   
<br>   

## 동적으로 요소 추가하기 (2)

<br>   

```javascript
let menus = [
    {name : '아메리카노', price: 3000},
    {name : '카페 라떼', price: 3500},
    {name : '에이드', price: 4000}
];

document.addEventListener("DOMContentLoaded", () => {
    const wrap = document.querySelector("#wrap");

    menu.forEach((item, index) => {
        const newDiv = document.createElement("div");
        newDiv.setAttribute("class", "box");

        const newH3 = document.createElement("h3");
        newH3.textContent = item.name;
        newDiv.appendChild(newH3);

        const newP = document.createElement("p");
        newP.textContent = `${item.price}원`;
        newDiv.appendChild(newP);

        wrap.appendChild(newDiv);
    })
})
```

<br>   
<br>   
