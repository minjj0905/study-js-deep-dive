## Quiz
- 진행자 : 박진아
- 날짜 : Aug 15 2023 
---
<!--
1. 질문은 이해하기 쉽고 명확하게 적는다.
2. 문제는 아래의 예시를 참고해 작성한다.
3. 문제의 정답은 주석으로 표기한다.
-->

> 1. 단항 산술 연산자는 부수 효과를 일으키지 않는다? (O/X)
```jsx
var x = 1;
x++;
console.log(x);
```
<!--
O 단항 산술 연산자는 부수 효과를 일으킵니다.
x에서는 암묵적 할당이 일어나 2가 됩니다.
-->

> 2. 다음 출력 결과는 어떻게 될까요? 
```jsx
let x;
const foo = true ? x = 'hi' : 'bye';
console.log(foo); // ?
console.log(x); // ?
```
<!--
할당 연산자는 평가 결과를 좌항에 있는 변수에 할당합니다.
그러므로 삼항연산자의 x = 'hi'는 평가 결과인 'hi'가 되므로
foo에는 'hi'가 할당됩니다.
```jsx
let x;
const foo = true ? x = 'hi' : 'bye';
console.log(foo); // 'hi'
console.log(x); // 'hi'
```
-->

> 3. 다음 출력 결과는 어떻게 될까요?
```jsx
for(var i = 1; i <= 10; i++){
  if (i % 2 == 0) continue;
  console.log(i);
}
```
<!--
```jsx
// 홀수만 출력
1, 3, 5, 7, 9
```
-->

> 4. 암묵적 타입 변환이 무엇일까요? 
<!--
암묵적 타입 변환은 js엔진이 타입을 변환 하는 것입니다. js엔진은 코드 문맥에 따라 타입을 변환합니다.
-->

> 5. 암묵적 타입 변환의 문자열, 숫자, 불리언 세가지 예시를 들어주세요
<!--
문자열 타입 변환은 `+` 문자열 연결 연산자 1+'2'로 타입 변환을 합니다.
숫자 타입 변환은 산술자 연산 1-'1'으로 타입 변환을 합니다.
불리언 타입 변환은 if문의 조건식의 조건 평과를 불리언 타입으로 암묵적 타입 변환을 합니다.
-->

> 6. 실제 결과와 주석이 틀린부분을 찾아주세요
```jsx
!! false; // false
!! null; // false
!! 0; // false
!! []; // false
!! {}; // false
```
<!--
빈 배열과 객체는 Truthy한 값으로 평가됩니다.
```jsx
!! []; // false -> true
!! {}; // false -> true
```
-->
