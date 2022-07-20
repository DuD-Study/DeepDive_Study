# Chapter 11

<pre>1. [     ]란 마치 배열처럼 인덱스로 프로퍼티 값에 접근할 수 있고 length프로퍼티를 갖는 객체를 말한다.
</pre>

<details>
  <summary>Solution</summary>
    <strong>유사 배열 객체</strong> : 문자열은 유사배열 객체이며 for문으로 순회할 수 있다.
</details>

<br>

<pre>2. 변수 str과 for문을 사용하여 다음과 같은 결과로 출력하시오.
</pre>

```js
let str = "hello";
```

결과

<pre>
h
e
l
l
o
</pre>

<details>
  <summary>Solution</summary>
  <pre>for(let i = 0; i < str.length; i++) {
  console.log(str[i]);
}
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

<pre>4. 얕은 복사가 가능한 조건은?
</pre>

<details>
  <summary>Solution</summary>
    <strong>깊이가 1단계 일때 </strong> 
</details>

<br>
