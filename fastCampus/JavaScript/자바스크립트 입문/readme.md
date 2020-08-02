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

1-4 연산자
-----------------------
* 산술 연산자
```javascript
let a = 1 + 2;
console.log(a); //-> 3
a = 2 - 1; // -> 1
a = 1 * 4; // -> 4
a = 4 / 2; // -> 2
```
* 전위, 후위
```javascript
let a = 1;
console.log(++a); //-> 2
a = 1;
console.log(a++); //-> 1
```

* 다른언어와 마찬가지 표현도 가능
```javascript
let a = 1;
a += 3;
a -= 3;
a *= 3;
a /= 3;
console.log(a)
```

1-5 논리 연산자
----------------
* 다른 언어와 마찬가지로 논리연사자 표현
```javascript
// 표현 순서는 연산자 우선순위 
// NOT ! -> 원래값에 반대로 ture-> false, false -> true
// AND && -> 둘다 참일 경우 true
// OR || -> 하나라도 참일경우 true
```

1-6 비교 연산자 
-------------------------
* === 과 == 
```javascript
const a = 1;
const b = 1;
const c = '1';
const equals = a === b ; // -> true
const equals2 = a == c; // -> true 
// === 타입까지 비교하는 연산 
// == 타입을 비교하지 않음 -> 실수 할수있으므로 ===로 되도록 사용
```

* !== 는 두 값이 다를때 사용 

* 기존 비교 연사자는 다른 언어와 동일
```javascript
// a < b;
// a <= b;
// a > b;
// a >= b;
```

1-7 조건문
---------------------------
* 조건이 참일때 실행된다 
```javascript
const a = 1;
if(a === 1){
  console.log("참입니다");
}
```

* 스코프가 다르면 선언가능 
```javascript
const a = 1;// 밖 스코프의 a
if(a + 1 === 2){
  const a = 2; // if문 안의 a
  console.log('if문 안의 a 값은 ' + a); // 2
}
console.log('if문 밖의 a 값은 ' + a); // 1
```

* if, else
```javascript
const a = 10;
if( a > 15 ){
  console.log('a가 15보다 큽니다');
} else{
  console.log('a가 15보다 크지 않습니다');// 이코드가 실행
}
```

* if ,else if, else
```javascript
const a = 10;
if( a === 15 ){ // 첫번째 조건판별
  console.log('a가 15 입니다');
}
else if( a === 10 ){ // 두번째 조건 판별
  console.log('a가 10 입니다');
} 
else{ // 마지막 조건 판별 
  console.log('a가 15와 10도 아닙니다.');
}
```

1-8 switch 
----------------------
* switch case 문
```javascript
const device = 'iphone' 

switch(device) { // 
  case 'iphone' :
    console.log('아이폰');
    break; // break가 없을시 다음 케이스 문 자동 실행
  case 'ipad' :
    console.log('아이패드');
    break;
  case 'galaxy' :
    console.log('갤럭시');
    break;
  default: // 위 모든 케이스가 아닌경우 
    console.log('아무것도 아님');
}
```

1-9 함수
------------------------
* 특정 기능을 수행하는 것
* input(파라미터)을 통하여 output(결과) 제공
* 함수는 function이라는 키워드 사용
```javascript
function add(a,b){ // 파라미터가 여러개일경우()로 구분 
  return a + b; // 결과값 반환은 return 
}
const sum = add(1,2);
console.log(sum); //=> 3결과값 
```
* 함수 사용
```javascript
function hello(name){
  console.log('hello '+ name+ '!');
}
hello('홍길동'); // 콘솔 결과창 hello 홍길동!
```
* 함수는 return 시 종료된다
```javascript
function hello(name){
 return 'hello '+ name+ '!' // 여기서 함수 종료

 console.log('test'); // 이코드부터 아래 코드는 동작 x 
 return;// 동작 x 
  
}
const test = hello('홍길동');
console.log(test); // 콘솔 결과창 hello 홍길동!
```


1-10 함수- Template Literal
----------------------------
* ES6 = ECMAScript6 = ES2015
* ` (백틱)문자를 사용하여 Template Literal 사용
```javascript
function hello(name){
  console.log(`hello ${name}`);
}
hello('홍길동'); // 콘솔 결과창 hello 홍길동!
```

1-11 화살표 함수(es6)
------------------------------
* 화살표 함수 사용법 (=>)
```javascript
const add = (a,b) => {
  return a + b;
}
const hello = (name) =>{
  console.log(`hello ${name}`);
}
const sum = add(1,2);
console.log(sum);
hello('홍길동');
```

* 화살표함수 사용법 (짧은 코드)
```javascript
const add = (a,b) => a + b;
const sum = add(1,2);
console.log(sum);
``` 

* function과의 차이점은 this차이 

1-11 객체
---------------------------
* 하나의 이름에 여러개의 값들을 선언가능
* 키 : 벨류 형태로 되어있음 ( key : value ) 
```javascript
const dog = {
  name: '멍멍이', // 쉽표로 구분해줘야 된다 
  age: 2,
  cute: true,
  sample: {
    a: 1,
    b: ,
  }
}
console.log(dog); // 객체정보
console.log(dog.name); // 멍멍이
console.log(dog.age); // 2
```

* 키값에는 숫자가 들어가긴하지만 보통 문자열로 선언 
* 문자열에는 공백이 있으면 안된다(선언하고 싶다면 따옴표(')로감싸줘야된다)
```javascript
const dog ={
  key with space : 'test' // 동작 x
  'key with space' : 'test' // 이렇게 써야된다
}
```

* 함수와 같이 사용 
```javascript
const ironMan = {
  name: '토니 스타크',
  actor: '로버트 다우니 주니어',
  alias: '아이언맨'
}

const captinAmerica = {
  name: '스티븐 로저스',
  actor: '크리스 에반스',
  alias: '캡틴 아메리카'
}

function print(hero){ // hero파라미터를 받아서 
  const text = `${hero.alias}(${hero.name}) 역학을 맡은 배우는 ${hero.actor} 입니다`
  console.log(text); // 출력 
}
print(ironMan);
print(captinAmerica);
```

* 객체 비구조화 할당 (객체 구조 분해)
```javascript
const ironMan = {
  name: '토니 스타크',
  actor: '로버트 다우니 주니어',
  alias: '아이언맨'
}

const captinAmerica = {
  name: '스티븐 로저스',
  actor: '크리스 에반스',
  alias: '캡틴 아메리카'
}
// 첫번째 방법
function print(hero){ 
  const { alias, name, actor } = hero;
  const text = `${alias}(${name}) 역학을 맡은 배우는 ${actor} 입니다`
  console.log(text);
}
// or 두번째 방법 
function print({ alias, name, actor }){ 
  const text = `${alias}(${name}) 역학을 맡은 배우는 ${actor} 입니다`
  console.log(text);
}
print(ironMan);
print(captinAmerica);
```

* 객체 안에 함수선언
```javascript 
const dog = {
  name: '멍멍이',
  sound: '멍멍!',
  say: function say(){
    console.log(this.sound); // 함수가 위치한 객체 자기 자신을 뜻함(this) === dog 
  }, // or
  say() {
    console.log(this.sound);
  }, // 아래 코드는 동작 x(화살표 함수)
  say: () => {
    console.log(this.sound); // -> this의 스코프가 달라짐 
  }
}

dog.say(); 
```

* getter / setter 
* getter함수
```javascript
const numbers = {
  a: 1,
  b: 2,
  get sum() { //getter의 경우 get으로 선언 -> 어떤 값을 무조건 반환해야된다 
    console.log('sum 함수가 실행됩니다!');
    return this.a + this.b;
  }
}

console.log(numbers.sum); // 3출력
```

* setter함수 
```javascript
const dog= {
  _name: '멍멍이',
  get name() {
  set name(value){ //setter함수의경우 파라미터를 받아야된다 
    console.log('이름이 바뀝니다 !' + value);
    this._name = value;
  }
};

console.log(dog._name);
dog.name = '뭉뭉이';
console.log(dog._name); // 이름이 뭉뭉이로 출력
```

* getter 와 setter 함수 활용
```javascript
const numbers = {
  _a: 1,
  _b: 2,
  sum: 3,
  calculate() {
    console.log('calculate');
    this.sum = this._a + this._b;
  },
  get a() {
    return this._a;
  },
  get b() {
    return this._b;
  },
  set a(value) {
    this._a = value;
    this.calculate();
  }
  set b(value){
    this._b = value;
    this.calculate();
  }
};

console.log(numbers.sum);
numbers.a = 5; 
numbers.b = 7;
numbers.a = 9;
console.log(numbers.sum); // 결과값 16 a: 9, b: 7
```
