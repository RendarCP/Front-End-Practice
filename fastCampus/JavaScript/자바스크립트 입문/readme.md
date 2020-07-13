JavaScript 입문 
==============
1-1 소개
---------------------------
* 모든 강의는 패스트캠퍼스 프론트엔드 강좌를 기반으로 작성
* 현재 강의는 <https://learnjs.vlpt.us/> 참조가능 

1-2 JavaScript
-----------
* 자바스크립트의경우 웹 브라우저 콘솔로 실행가능 
* 웹 브라우저상에서 매번 하기엔 힘듬 
* <https://codesandbox.io>에서 create sandbox -> Vanilla 선택 

1-3 변수
----------------------
* 변수 선언시에는 let이라는 콘텍스트 사용 
```javascript
let value = 1; //log(1)
vale = 2; //log(2)
```
  * 한번 초기화된 변수명은 다시 초기화할수 없다 
  ```javascript
  let value = 1;
  let value = 2;
  // SyntaxError 
  ```
* 상수 선언시에는 const라는 콘텍스트 사용 (한번 초기화시 값 변경할수없다)
```javascript
const a = 1; 
a = 2; // -> "a" is read Only 
const a = 2; // 마찬가지로 a가 선언된 상태에서 다시 못함(변수랑 상수 동일)
```
* var라는 키워드도 존재하지만 권장하지는 않음 (몰라도됨)
```javascript
var a = 1;
var a = 2;
//이렇게 사용가능 
```
* 문자열 선언
```javascript
let text = 'hello'; // 작은따옴표
let name = "헬로우"; // 큰 따옴표
// 둘의 차이는 없음(취향차이) 
```

* boolean값 
```javascript
let text = true; // 참
let name = false; // 거짓
```

* 값이 존재하지 않을경우 
```javascript
let text = null; // 값이 아예 없음
let name = undefined; // 아직 값이 정해지지않음 
```

