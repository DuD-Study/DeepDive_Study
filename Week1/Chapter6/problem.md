# Chapter 6

<pre>1. 변수 선언에 의해 확보된 메모리 공간을 처음 할당이 이뤄질 때까지 빈상태로 내버려두지 않고 자바스크립트 엔진이 <br>1.[         ]로 초기화 한다. 하지만 변수값이 아예 없다는 걸 명시하고 싶을때는 2.[       ]을 할당하면 된다.
</pre>

   <details>
      <summary>Solution</summary>
        <strong>1.undefined, 2.null</strong>
        
   </details> 

<br>
<br>
<br>



<pre>2. 자바스크립트의 변수는 선언이 아닌 할당에 의해 타입이 결정된다. 그리고 재할당에 의해 변수의 타입은 언제든지 동적으로 변할 수 있다. <br>이러한 '특징'을 [         ]이라 한다. </pre>

   <details>
      <summary>Solution</summary>
        <strong>동적타이핑</strong>
   </details> 


<br>
<br>
<br>

<pre>3. 다음은 변수 사용시 주의할 사항입니다. 빈칸을 채워 보시오.

 1. [       ]는 꼭 필요한 경우에 한해 제한적으로 사용한다. 동적 타입 언어 특성상 타입을 잘못 예측해 오류가 발생할 가능성이 높기 때문이다. 
 2. 변수의 [         ]를 최대한 좁게 만들어 변수의 부작용을 억제해야 한다. 
 3. 어디서든 참조/변경 가능한 [       ]는 의도치 않게 값이 변경될 가능성이 높고 다른 코드에 영향을 줄 가능성도 높기때문에 최대한 지양해야한다.
 4. 변수보다는 [       ]를 사용해서 값의 변경을 억제한다. 
 5. 변수의 목적이나 의미를 파악할 수 있도록 변수 이름에 [      ]한다.
 </pre>

   <details>
      <summary>Solution</summary>
        <strong>변수, 스코프(유효범위), 전역변수, 상수, 네이밍</strong>
   </details>

<br>

<pre>4. 모든 변수에 암묵적으로 할당되는 값은? </pre>

   <details>
      <summary>Solution</summary>
        <strong>Undefined</strong>
   </details> 

<br>

<pre>5. 표현식을 삽입하는 방법은? </pre>

   <details>
      <summary>Solution</summary>
        <strong> 템플릿 리터럴 내에서 ${} 으로 감싼다</strong>
   </details> 