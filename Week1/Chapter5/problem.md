# Chapter 5 

<pre>1. 자바스크립트 엔진이 소스코드를 해석할 때 문의 끝이라고 예측되는 지점에 세미콜론을 자동으로 붙여주는 [        ]이 암묵적으로 수행된다. 
</pre>

   <details>
      <summary>Solution</summary>
        <strong>세미콜론 자동 삽입 기능(ASI)</strong> - automatic semicolon insertion
        
   </details> 

<br>
<br>
<br>




<pre>2. 표현식과 표현식이 아닌문 골라주세요.</pre>

```js
let x;
1+2
t = 3 * 3 

```


   <details>
      <summary>Solution</summary>
        <strong>let x;</strong>는 표현식이 아니다. 표현식 구분은 간단하다. 변수에 할당해 보는 것인다.<br>할당 할 수 없을거 같은 건 표현식이 아닌거다.
   </details> 


<br>
<br>
<br>

<pre>3. 다음 실행결과를 예측해보세요.</pre>

```js
f1();

function f1(){
  console.log(y);
  function f2(){
    var y = 2;
    function f3(){
      console.log(y);
    }
    f3();
  }
  f2();
}
```


   <details>
      <summary>Solution</summary>
        <strong>y is not defined</strong> 외부에서 내부 함수의 변수는 접근 불가하다.
   </details> 