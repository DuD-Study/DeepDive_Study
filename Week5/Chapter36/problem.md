# Chapter 36

<pre>1. 아래 문장으로 나오게끔 객체 디스트럭처링해보세용</pre>

```js
const favSinger = {
  name: "Shawn Mendes",
  age: 25,
  nationality: "Canada",
  Hitsongs: {
    playList1: "Handwritten",
    playList2: "Illuminate",
    playList3: "Wonder",
  },
};

const {} = favSinger;
console.log();

console.log(
  "저의 최애 가수는 Shawn Mendes고, Canada출신 가수입니다. 그리고 Handwritten이라는 앨범으로 인지도가 엄청오르게 됩니다."
);
```

<details>
  <summary>Solution</summary>

```js
// 중첩 객체를 디스트럭쳐링하려면 부모 키값 : { 원하는 중첩객체 value의 키값 }
const {
  name,
  nationality,
  Hitsongs: { playList1 },
} = favSinger;

console.log(
  `저의 최애 가수는 ${name}고, ${nationality}출신 가수입니다. 그리고 ${playList1}이라는 앨범으로 인지도가 엄청오르게 됩니다.`
);
```

</details>

<br>

<br>

<pre>2. todos에 디스트럭처링을 사용하여 'REACT' 출력 값이 나오게 하세요. </pre>

```js
const todos = [
  { id: 1, content: "HTML", completed: true },
  { id: 2, content: "CSS", completed: false },
  { id: 3, content: "REACT", completed: true },
];
// 코드

console.log(content); // 'REACT'
```

<details>
<summary>Solution</summary>

```js
const [, , { content }] = todos;
console.log(content); // 'REACT'
```

</details>
