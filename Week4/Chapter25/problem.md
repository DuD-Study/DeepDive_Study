# Chapter 25

<pre>1. 다음 생성자 함수를 클래스로 만들어보자, 똑같이  </pre>


```js
function Intro(name,MBTI){
  this.name = name;
  this.MBTI = MBTI;

  Intro.prototype.sayHi = function () {
      console.log(`Hi my name is ${this.name}, and btw What's your MBTI? mine is ${this.MBTI}`)
  }
}

const me = new Intro('jeongmin', 'ESTP');
me.sayHi();
```


<details>
  <summary>Solution</summary>

```js
class Intro {
    constructor(name, MBTI){
    this.name = name
    this.MBTI = MBTI
    }

    sayHi() {
         console.log(`Hi my name is ${this.name}, and btw What's your MBTI? mine is ${this.MBTI}`)
    }
}

const me = new Intro('jeongmin', 'ESTP');
me.sayHi();
```
</details>

<br>
