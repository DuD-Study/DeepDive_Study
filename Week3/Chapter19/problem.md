<pre>1. 아래의 빈칸을 알맞은 단어로 채우시오.</pre>
<div align="center">
객체는 [①] 데이터와 [②]을 하나의 논리적인 단위로 묶은 복합적인 자료구조라고 할 수 있다.
이때 객체의 [①]를 [③], [②]를 [④]라 부른다.
</div>

<details>
<summary>Solution</summary>
<strong>①: 상태<br>②: 동작<br>③: 프로퍼티<br>④: 메서드</strong>
</details>

<pre>2. 다음 코드의 실행결과를 예측해보시오.</pre>
```js
const obj = {};
const parent = {x : 1};

Object.setPrototypeOf(obj, parent);

console.log(obj);
```

<details>
<summary>Solution</summary>
<strong>{}</strong>
<pre>obj의 프로토타입에 x: 1이 추가 되는 것이지 obj 자체가 변하는 것은 아니다.
위의 코드에서 Object.getPrototypeOf(obj)를 실행해보자.</pre>
</details>


