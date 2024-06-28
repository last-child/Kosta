## 컴포넌트 (1)

<br>   

```jsx
import React from "react";

function Book(props) {
  return (
    <ul>
      <li>제목: {props.title}</li>
      <li>저자: {props.author}</li>
      <li>단행본 : {props.series}</li>
    </ul>
  );
}

export default Book;
```

<br>   

```jsx
import React from "react";
import Book from "./Book";

function Library() {
  return (
    <div>
      <Book title="나루토" author="키시모토 마사시" series={50} />
      <Book title="원피스" author="오다 에이치로" series={109} />
      <Book title="블리치" author="쿠보 타이토" series={38} />
    </div>
  );
}

export default Library;
```

<br>   

+ 상위 컴포넌트(Library)는 하위 컴포넌트(Book)에 데이터(title, author, series)를 전달한다.
+ 하위 컴포넌트(Book)는 전달받은 데이터(title, author, series)를 이용하여 UI를 렌더링한다.

<br>   
<br>   
<br>   
<br>   
<br>   

## 컴포넌트 (2)

<br>   

```jsx
import React from "react";
import Book from "./Book";

function Library() {
  const books = [
    {title: "나루토", author: "키시모토 마사시", series: 50},
    {title: "원피스", author: "오다 에이치로", series: 109},
    {title: "블리치", author: "쿠보 타이토", series: 38},
  ];

  return (
    <ul>
      {books.map((book, index) => (
        <Book key={index} title={book.title} author={book.author} series={book.series} />
      ))}
    </ul>
  );
}

export default Library;
```

<br>   

+ 상위 컴포넌트(Library)는 map 메서드를 통해 하위 컴포넌트(Book)를 동적으로 생성한다.
+ 하위 컴포넌트(Book)에 key를 비롯한 여러 데이터들이 속성(props)으로 전달된다.
