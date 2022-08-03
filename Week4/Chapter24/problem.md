# Chapter 24

<pre>1. 모든 함수는 상위 스코프를 기억하므로 이론적으로 모든 함수는 클로저인데,
   일반적으로 모든 함수를 클로저라고 하지 않는다. 다음 코드를 보고 클로저가 아닌 이유는 ?</pre>

```js
function foo() {
      const x = 1;
      const y = 2;

      function bar() {
        const value = 3;
        console.log(2*value);
      }

      return bar;
    }

    const getDouble = foo();
    getDouble();
```



<details>
  <summary>Solution</summary>
  <pre>중첩함수가 외부함수, 즉 상위 스코프 식별자를 참조하지 않으면 클로저라고 하지않는다.</pre>
</details>

<br>
