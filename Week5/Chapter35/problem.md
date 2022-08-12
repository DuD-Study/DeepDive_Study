# Chapter 35

<pre>1. 아래 예상 출력 결과대로 나오는지 예상해보시고, 아니라면 어떻게 해줘야하는지 생각해봅시다.</pre>

```js
var arr1 = [1, 2];
var arr2 = [3, 4];
var arr3 = [5, 6];

const answer1 = arr1.concat(arr2);
const answer2 = [...answer1];
answer2.splice(4, 0, arr3);
const answer3 = [...answer2];

console.log(answer1); // 1. [1,2,3,4]
console.log(answer2); // 2. [1,2,3,4,5,6]
console.log(answer3); // 3. [1,2,3,4,5,6]
console.log(answer2 === answer3); // 4. true
```

<details>
  <summary>Solution</summary>
  <strong>
  1. [1,2,3,4] <br>
  2. [1,2,3,4,[5,6]] <br>
  3. [1,2,3,4,[5,6]] <br>
  4. false <br>
  </strong>
  <pre>
  1) 두개의 배열을 합칠때는 concat 메소드를 사용합니다. 하지만 스프레드 연산으로 바꿔볼 수 있겠죠.
  
  ```js
  const temp = [...arr1, ...arr2];
  ``` 
  2) splice() 메소드를 매개변수 3개를 받는데 첫번째 인자가 자르기 시작할 인덱스 두번째 인자가 
     그 시작하는 인덱스에서 몇개나 자를지, 그리고 3번째 인자는 2번째로 나간자리를 메울 것을
     넣어줍니다. 하지만 예상한 값과 다르죠? 왜냐하면 저희는 배열자체를 넣어 버렸으니까요.   
     분해를 해줘야하는데, ES5때는 저렇게 분해하기위해 복잡한 메소드체이닝을 통해 전달해 주었다면,
     이번 챕터에서 배운 스프레드 문법을 주면 이렇게 쉽게 저런 문제가 해결됩니다...
  ```js
  Array.prototype.splice.apply(answer2,[4,0].concat(arr3)); //[1,2,3,4,5,6]
  answer2.splice(4,0, ...arr3); //[1,2,3,4,5,6]
  ```
  3) answer3에 answer2를 slice()로 얕은복사하는 거죠.하지만 스프레드 문법으로 한다면
  ```js
  const answer3 = [...answer2];
  ```
  4) 얕은 복사였기 때문에 답은 false
  </pre>
  </details>

<br>

<pre>2. 아래 출력값을 나타내는 함수를 만들어보자 (매개변수, rest param을 사용하지않고 Spread문법사용)</pre>

```js
console.log(intro("Kyle", 28)); // 안녕하세요 저는 Kyle이고 28살입니다.
```

<details>
<summary>Solution</summary>

```js
function intro() {
  const [name, age] = [...arguments];
  return `안녕하세요 저는 ${name}이고 ${age}살입니다.`;
}
```

</details>

<br>

<pre>3. 아래 출력 값을 작성하고, 스프레드 문법을 사용하여 만들어보자. </pre>

```js
const obj = { x: 1, y: 2 };
const copy = Object.assign(obj, { y: 3, z: 4 });
console.log(copy);
```

<details>
<summary>Solution</summary>
<pre>출력 : {x: 1, y: 3, z: 4}</pre>

```js
const copy = { ...obj, ...{ y: 3, z: 4 } };
console.log(copy); // {x: 1, y: 3, z: 4}
```

</details>

<pre>4. 아래 코드의 결과는? </pre>

```js
const whiteWater = {
  name: '흰색물',
  attribute: '물',
  color: '흰색'
};

const { color, ...water } = whiteWater;
console.log(color);
console.log(water);

const { attribute, ...pureName } = water;
console.log(attribute);
console.log(pureName);
```

<details>
<summary>Solution</summary>

```js
흰색 // whiteWater안에 color를 출력
{ name: '흰색물', attribute: '물' } //color을 제외한 나머지 출력
물 // attribute를 출력
{ name: '흰색물' } //attribute를 제외하고 출력
```
</details>
