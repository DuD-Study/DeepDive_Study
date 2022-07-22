# Chapter 11

<pre>1. [     ]란 마치 배열처럼 인덱스로 프로퍼티 값에 접근할 수 있고 length프로퍼티를 갖는 객체를 말한다.
</pre>

<details>
  <summary>Solution</summary>
    <strong>유사 배열 객체</strong> : 문자열은 유사배열 객체이며 for문으로 순회할 수 있다.
</details>

<br>

<pre>2. 다음 코드의 실행 결과를 예측해 보시오.
</pre>

```js
const person1 = {
    name: "Lee",
}

const person2 = {
    name: "Lee",
}

console.log(person1 === person2); // ①
console.log(person1.name === person2.name); // ②
```



<details>
  <summary>Solution</summary>
  <pre>
① = false (person1과 person2는 내용은 같지만 다른 메모리에 저장된 별개의 객체임. (원시 값이 아님))
② = true (두 표현식 모두 원시값 "Lee"로 평가되기 때문.)
</pre>
</details>

<br>

<pre>3. 원시 값을 변경하려면은?
</pre>

<details>
  <summary>Solution</summary>
    <strong>재할당 한다.(새로운 메모리에 할당)</strong> <br> ex) let test = "test"<br> test = "change test"
</details>

<br>

<pre>4. 원시 값을 변수에 할당하면 변수에는 [     ]이 저장된다. 이에 비해 객체를 변수에 할당하면 변수에는 [     ]이 저장된다.
</pre>

<details>
  <summary>Solution</summary>
    <strong>실제 값, 참조 값</strong> 
</details>

<br>
