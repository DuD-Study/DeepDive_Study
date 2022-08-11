# Chapter 34


<pre>1. 밑에 코드를 참고해서 for ... of의 내부 동작을 표현해봅시다.</pre>

```js
// 배열은 이터러블 프로토콜을 준수한 이터러블이다.
const array = [1, 2, 3];

// Symbol.iterator 메서드는 이터레이터를 반환한다. 이터레이터는 next 메서드를 갖는다.
const iterator = array[Symbol.iterator]();

// next 메서드를 호출하면 이터러블을 순회하며 순회 결과를 나타내는 이터레이터 리절트 객체를
// 반환한다. 이터레이터 리절트 객체는 value와 done 프로퍼티를 갖는 객체다.
console.log(iterator.next()); // { value: 1, done: false }
console.log(iterator.next()); // { value: 2, done: false }
console.log(iterator.next()); // { value: 3, done: false }
console.log(iterator.next()); // { value: undefined, done: true }
```

```js
const iterable = [1, 2, 3];
const iterator = iterable[Symbol.iterator]();

for (;;) 
{
  // 여기 안에 코드 
}
```

<details>
  <summary>Solution</summary>
  <pre>for ... of문은 내부적으로 이터레이터의 next 메소드를 호출하여 이터러블을 순회하며
반환한 이터레이터 result 객체의 value 프로퍼티를 for ... of문의 변수로 할당한다고 합니당.</pre>

  ```js
// 이터러블
  const iterable = [1, 2, 3];
  const iterator = iterable[Symbol.iterator]();

  for (;;) {
  // 이터레이터의 next 메서드를 호출하여 이터러블을 순회한다. 이때 next 메서드는 이터레이터 리절트 객체를 반환한다.
  const res = iterator.next();

  // next 메서드가 반환한 이터레이터 리절트 객체의 done 프로퍼티 값이 true이면 이터러블의 순회를 중단한다.
  if (res.done) break;

  // 이터레이터 리절트 객체의 value 프로퍼티 값을 item 변수에 할당한다.
  const item = res.value;
  console.log(item); // 1 2 3
  }
  ```
  
</details>  

<br>