# Chapter 17

<pre>1. 객체 리터럴에 의한 객체 생성 방식은 직관적이고 편하다. 하지만 왜 비효율 적인가 ?</pre>

```js
const circle1 = {
  radius: 5,
  getDiameter() {
    return 2 * this.radius;
  }
};

console.log(circle1.getDiameter()); // 10

const circle2 = {
  radius: 10,
  getDiameter() {
    return 2 * this.radius;
  }
};

console.log(circle2.getDiameter()); // 20
```

<details>
  <summary>Solution</summary>
  <strong>동일한 프로퍼티를 갖는 객체를 여러 개 생성해야하는 경우 매번 같은 프로퍼티를 기술해야하기 때문입니다.</strong>
</details>

<br>
