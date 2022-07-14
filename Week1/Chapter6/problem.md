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
<br>
   <pre>6. 자바스크립트의 숫자 타입은 정수만을 위한 타입이 없고 모든 수를 [  ]로 처리하는데 이는 정수로 표시 된다 해도 사실은 [  ]라는 것을 의미합니다. 따라서 정수로 표시되는 수끼리 나누더라도 [  ]가 나올 수 있습니다.
</pre>

<details>
   <summary>Solution</summary>
      <strong>실수</strong>
</details>

<br>

<pre>7. ES6부터 템플릿 리터럴이라고 하는 새로운 문자열 표기법이 도입되었으며, 템플릿 리터럴은 멀티라인 문자열, 표현식 삽입, 태그드 템플릿 등 편리한 문자열 처리 기능을 제공합니다. 템플릿 리터럴은 런타임에 일반 문자열로 변환되어 처리되는데, 템플릿 리터럴은 일반적은 따옴표 대신 [  ]을 사용해 표기합니다.
</pre>

<details>
   <summary>Solution</summary>
      <strong>백틱(``)</strong>
</details>

<br>

<pre>8. [  ]은 변수에 값이 없다는 것을 의도적으로 명시(의도적 부재)할 때 사용합니다. 함수가 유효한 값을 반환할 수 없는 경우 명시적으로 [  ]을 반환하기도 합니다. 예를 들어, HTML요소를 탐색해 반환하는 documents.querySelector 메서드는 조건에 부합하는 HTML 요소를 검색할 수 없는 경우 에러 대신 [  ]을 반환합니다. 
</pre>

<details>
   <summary>Solution</summary>
      <strong>null</strong>
</details>

<br>
