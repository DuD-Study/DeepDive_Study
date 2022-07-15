# Chapter 4

<pre>1. 자바스크립트는 변수의 타입 지정없이 값이 할당되는 과정에서 자동으로 변수의 타입이 결정된는데 이를 [         ]언어라고 한다.
</pre>

   <details>
      <summary>Solution</summary>
        <strong>동적타입</strong>
        
   </details>

<br>

<pre>2. 변수에 값을 할당하지 않으면 어떤 값이 할당되는가?
</pre>

   <details>
      <summary>Solution</summary>
        <strong>undefined</strong>
   </details>

<br>

<pre>3. 호이스팅의 의미를 설명하시오.</pre>

   <details>
      <summary>Solution</summary>
   <strong>호이스팅</strong>이란 선언문이 코드의 <strong>선두</strong>로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징을 뜻한다.
   </details> 
   
<br>

<pre>4. 선언과 할당의 실행시점의 차이를 설명하시오.</pre>

   <details>
      <summary>Solution</summary>
   선언은 소스코드가 순차적으로 실행되는 시점인 런타임 이전에 먼저 실행되고, 할당은 런타임에 실행된다.
   </details> 
   
<br>

<pre>5. Hello World를 camel case, snake case, pascal case를 이용하여 표현하시오.</pre>

<details>
   <summary>Solution</summary>
   camel case = helloWorld<br>
   snake case = hello_world<br>
   pascal case = HelloWorld<br>
</details>

<br>

<pre>6. 변수 선언하는 3가지 방법은?  </pre>

   <details>
      <summary>Solution</summary>
      <strong> var, let, const</strong>
   </details>

<br>
<pre>7. 값을 재할당할 수 있는건 [    ] 저장된 값을 변경할 수 없으면 [    ]  </pre>

   <details>
      <summary>Solution</summary>
      <strong> 변수,  상수</strong>
   </details>

<pre>8. [   ]는 변수 이름이라고도 하며 어떤 값을 구별해서 [  ]할 수 있는 고유한 이름입니다. <br>값이 아니라 메모리 주소를 기억하고 있어 메모리 주소를 통해 메모리 공간에 저장된 값에 접근할 수 있습니다. 즉, 이것은 메모리 주소에 붙인 이름 입니다.
</pre>

<details>
   <summary>Solution</summary>
      <strong>식별자</strong>
</details>

<br>

<pre>9. [   ]은 변수 생성을 의미하는데, 값을 저장하기 위한 메모리 공간을 확보하고 변수 이름과 확보된 메모리 공간의 주소를 연결해서 값을 저장할 수 있게 준비하는 것 입니다.<br> [  ] 이후 변수에 값이 할당되지 않은 상태일 경우 자바스크립트 엔진에 의해 undefined가 암묵적으로 할당되어 초기화 됩니다.
</pre>

<details>
   <summary>Solution</summary>
      <strong>변수 선언</strong>
</details>

<br>

<pre>10. 변수 이름을 비롯한 모든 식별자는 [   ]에 등록되는데, [   ]는 자바스크립트 엔진이 소스 코드를 평가하고 <br>실행하기 위해 필요한 환경을 제공하고 코드의 실행 결과를 실제로 관리하는 영역입니다. 
</pre>

<details>
   <summary>Solution</summary>
      <strong>실행 컨텍스트</strong>
</details>

<br>

<pre>11. [   ]는 애플리케이션이 할당한 메모리 공간을 주기적으로 검사하여 더 이상 사용되진 않는 메모리를 해제하는 기능을 말합니다. <br>더 이상 사용되지 않는 메모리란 어떤 식별자도 참조하지 않는 메모리 공간을 의미합니다.<br> 자바스크립트는 이것을 내장하여 메모리 누수를 방지합니다.
</pre>

<details>
   <summary>Solution</summary>
      <strong>가비지 콜렉터(garbage collector)</strong>
</details>

<br>
