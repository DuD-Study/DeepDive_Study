# Chapter 10
<h2 align="center">JS를 구성하는 거의 "모든 것"이 객체다.</h2>
<br>

<pre>1. 아래 코드의 결과는? </pre>
```js
   var obejct1 = {};
   console.log(typeof empty);
```
   <details>
      <summary>Solution</summary>
        <strong>정답은 : Empty 
        <br>프로퍼티가 없어도 객체는 생성 됩니다.</strong><br>
   </details> 
<br>

<pre>2. 아래 코드의 결과는? </pre>
```js
   var person = {
      name : 'Kwon'
   }
   console.log(person.name);
   console.log(person['name']);
   console.log(person.age);
```
   <details>
      <summary>Solution</summary>
        <strong> 첫번째, 두번째 은 Kwon이 출력되지만<br> 
        <br>세번째는 객체에 존재하지 않는 프로퍼티에 접근해서 undefined가 반환됩니다.</strong><br>
   </details> 
<br>
