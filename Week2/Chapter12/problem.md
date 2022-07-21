# Chapter 12

<pre>1. 함수 내부로 입력을 전달받는 변수를 [       ], 입력을 [        ], 출력을 [           ]이라한다. </pre>

<details>
  <summary>Solution</summary>
    <strong>매개변수(Parameter), 인수(argument), 반환값(return value)</strong>
</details>

<br>

<pre>2. 함수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징을 함수 [       ]이라 한다. 
</pre>

<details>
  <summary>Solution</summary>
  <pre>호이스팅</pre>
</details>

<br>

<pre>3. 아래의 코드를 보고 실행 결과를 예측하시오.
</pre>

```js
(function foo() {
  console.log("hi");
});
foo(); // 1. ?
{
  function bar() {
    console.log("hello");
  }
}
bar(); // 2. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. ReferenceError: foo is not defined<br>2. hello</strong>
  <pre>그룹 연산자 () 내에 있는 함수 리터럴(foo)은 함수 선언문으로 해석되지 않고 함수 리터럴 표현식으로 해석된다. 그룹 연산자의 피연산자는 값으로 평가될 수 있는 표현식이어야 하기 때문에 함수선언문인 foo는 피연산자로 사용할 수 없다.</pre>
</details>

<br>

<pre>4. 함수의 매개변수를 통해 다른 함수의 내부로 전달되는 함수를 [1.     ],<br> 매개변수를 통해 함수의 외부에서 [1.     ]를 전달받은 함수를 [2.     ]라 한다. </pre>

<details>
  <summary>Solution</summary>
    <strong>1.콜백함수, 2.고차함수</strong>
</details>

<br>

<pre>5.함수 표현식과 함수 선언문 중 함수의 생성 시점이 빠른 것은?</pre>

<details>
  <summary>Solution</summary>
    <strong>함수 선언문</strong> : 자바스크립트 엔진에 의해 먼저 실행된다.
</details>

<br>

<pre>6. 함수형 프로그래밍은 함수 외부 상태의 변경을 지양하는 [     ]를 통해 부수효과를 최대한 억제해 오류를 피하고 프로그램의 안정성을 높이려는 노력의 일환이라고 볼 수 있다.</pre>

<details>
  <summary>Solution</summary>
    <strong>순수함수</strong> 
    <pre>외부 상태에 의존하지도 않고 변경하지도 않는 부수효과가 없는 함수를 순수 함수라고 하고, 외부 상태에 의존하거나 외부 상태를 변경하는, 즉 부수 효과가 있는 함수를 비순수 함수라고 한다. 함수가 외부 상태를 변경하면 상태 변화 추적이 어려워지므로 함수 외부 상태의 변경을 지양하는 순수 함수를 사용하는 것이 좋다.</pre>
</details>

<br>
