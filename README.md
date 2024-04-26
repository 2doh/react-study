# css 최적화

# js Syntax 1장

1. Syntax (구문) : 약속된 문법

2. Interpreter (번역 ) : 갤럭시 AI/웹브라우저

3. 프로그래밍은 요구사항을 분석하고, (개인별로 작성 : 의사코드 )
   Syntax 를 이용해서
   적절한 자료구조 + 적절한 함수를 활용하고,
   흐름을 제어하여 요구사항을 만족 시킨다.

# js 2장

```txt

  mp3  실행하려면? mp3 Player
  .hwp 실행하려면? 한글 Player

   javaScript 뭐지 ?


   publisher : 웹브라우저용 프로그래밍 언어 (html, css 다룬다)
   FE        : node.js (웹브라우저용 pg 아니고, pc 용 프로그래밍 언어)
               서버(dothome... db... html, css ...)

   웹 브라우저 player 마다 다 다르다.
   IE, Chrome, Opera, Safari..... (모두 다 다르다. Syntax )
   예) 메뉴하나를 만들어도 다시 각각에 웹브라우저에 맞게 마이그레이션을 해야.



   ES6

   렌더링 (목표는 html, css, js 로 문서 만들기)

    SSR (Server Side Redering)
     : php, spring (WAS), Next.js

    CSR (Client Side Redering) 이 있어요.
     : React, Vue, Angular ..

    Ajax (아작스, 에이젝스..) : 데이터(json) 통신
      : 비동기 (Request 요청  Response 회신) / 동기 구분
      : XML Http Request (XHR 통신)
      : vanila JS / pure JS (fetch/async await)     <=====>    jQuery (ajax)


      Node.js 하실 수 있나요?
       서버(Express.js), DB(MongoDB, MySql) 가능합니까?

      SPA : Single Page Application
      CBD : Component based Developement

      객체 지향
      : 모든 코드의 시작은 객체로 설계하여 전개한다.

      예) 기획자 : xls 로 제공한다.
          - 인터파크 상품(최상단 배치되는 제품의 정보를 노출)
          - 상품의 기본 정보
           : 할인율, 가격, 제목, 이미지 보여주면 되겠다.
           : 제품상세 정보로 이동하는 경로를 제공

          디자이너
          - UI 및 UX 배치

          BE 개발자
          - 제품의 정보를 DB 저장해둠. (일부만 Response )

          FE 개발자 :
          const Good = {
            ratio : 할인율,
            price : 가격,
            title : 제목,
            pic  : 이미지주소,
            link : 제품주소
          }

          const 객체명 = {
             속성명 : 속성값,
             기능   : function(){ 기능 }
          }


          Const TodoList = () => {
            const gogo = (e) => {
              alert ("클릭")
            }
            return (
               <>
                 <div className="a" onClick="gogo">
                   ~~~~
                  </div>
               </>
             )
          }


      프로토타입 기반 : 프로토타입(유전자)를 상속받아 덧댄다.

      Babel 이란 : 현재 최신 코드를 옛날 코드로 변환해 준다.


```

# js 3장

```txt
DOM(Document Object Model)
   - html 을 읽고, 수정 등등의 조작을 하는
     함수 (DOM API)
     document.querySelector(".wrap")

    클라이언트 사이드 API
    DOM, BOM, Canvas, XMLHttpRequest, fetch
    requestAnimationFrame, SVG, Web Storage,
    Web Component, Web Worker 등..

    Node.js   설치를 하면 자동으로
    npm 설치 됩니다. Node Package(js 소스) Manager
    https://www.npmjs.com/

    npm install 패키지명@버전
    node -v
    npm -v

    nvm (Node.js 의 버전을 자유롭게 변경하고, 설치)

    yarn install 패키지명@버전
```

# js 4장

- var 변수명 = 변수값;
- let 변수명 = 변수값;
- const 변수명 = 변수값;

```txt
   호이스팅(hoisting)은 변수, 함수를 선언하지 않았는데도 사용할수있음(hoisting이 일어나지 않도록 주의 : var 쓰지 말자)
```

# js 5장

```txt
코딩에서의 값 : 변수에 할당(보관한)된 결과 / 표현식이 평가(식을 해석해서 값을 생성하고 참조하는 것)된 결과를 말한다
변수 : 컴퓨터 공간에 이름을 붙여둔 방 한개

리터럴 : 사람이 이해할 수 있는 문자 혹은 약속된 기호를 사용해서 값을 생성하는 표기법
리터럴은 값을 평가해서 코드에 활용하기 위한 문법

표현식(experession) : 값으로 평가될 수 있는 모든 식

문(statement) : 프로그램을 구성하는 기본단위 / 최소 실행단위
```

# js 6장

```txt
데이터 타입  : 자료(JS의 리터럴로 처리될 수 있는)의 종류
타입(Type) : 자료의 형태

타입스크립트 : 데이터 종류를 표현해 주는 방식

원시타입
이를 모아 하나로 만들어낸 방식이 객체
1. 숫자타입
2. 문자열타입 : ' ' - 문자(한글자 ex) '5', 'a') / " " - 문자열(두글자 이상 ex) "15", "abcd"
2-1. 템플릿 리터럴 : ` ` - 들여쓰기, 줄내림 등 표현 가능   ex) "안녕     = 안녕반가워           `안녕     =   안녕
                                                             반가워"                          반가워`      반가워
   표현식(값을 만들어 리턴하는 식) 삽입 : 리터럴(` `) 내 ${} 를 통해 표현식 삽입 가능
ex) if. x= 만나서 / ` 안녕 ${x} 반가워 ` = 안녕 만나서 반가워
3. 불리언 타입 : true or false
4. undefined 타입 : 값을 정의하지 않았다(값을 모른다는 의미)
5. null타입 : 값이 없다(값이 진짜 비어있다는 의미)
6. 심볼타입


데이터타입 : 자료형
불변성(immutable) : 데이터 값 변경 X
원시데이터는 immutable한 데이터타입임
- number : 1 / string : 'a' / boolean : true, false / undefined : undefined / null : null / symbol : Symbol() 만들어진 값 변경불가
가변성(mutable) : 데이터 값 변경 O

복합형 데이터 객체
객체는 원시데이터를 모아서 저장하고 관리하는 것
if) const lee = { age:20, marry : true } 여기서 lee는 lee.age / lee.marry 총 두 가지의 값을 가진다. 즉, block {} 안의 속성 모두에 대한 값

동적 타이핑 : 자바스크립트는 동적이라 데이터타입을 스스로 분류함

반드시 알아야함
1. 데이터타입 : 자료(리터럴 값)의 종류
2. js에서는 값 리터럴에 따라 변수의 종류를 구별(타입을 추론)
3. 타입을 추측해서  타입을 변경
```

# js 7장

```txt
이 항 : 2개의 항목을 처리하는 연산자 값 만들기

- +  -  *  /  %(모듈러 연산자) : 나누고 난 후 나머지 값

단 항 : 1개의 항목을 처리하는 연산자 값 만들기

- ++   - -

글자도 더할 수 있다

ex) ‘1’ + 2 = 12

할당연산자

x = x+1 이 식을  x += 1 이렇게 표현할 수 있다

**비교연산자**

- == (같다)

if) 1 == ‘1’ (true) :  숫자와 글자의 비교 but 자바스크립트는 타입 변화를 통해 둘 다 숫자로 인식  - 오류의 원인이 될 수 있으므로 사용 자제

- === (같다)

if) 1 === ‘1’ (false) : 1. 데이터의 종류 비교 / 2. 데이터 값 비교

!== : 값과 데이터 형식 같은지 확인. 같은 경우 true / 아닐 경우 false

대소관계

- <    >    <=    >=

**삼항연산자**

- ? :  조건식을 기반으로 두 가지 중 하나의 표현식을 실행, 결과를 반환

ex) condition ? expressionIfTrue : expressionIfFalse : contdition이 true면 expressionIfTrue가 실행, false면 expressionIfFalse 실행

논리연산자

- || : OR 연산자 - 둘 중 하나 true ⇒ true
- && : AND 연산자 - 둘 다 true ⇒ true
- ! : NOT 연산자

그 외의 연산자

- ?. (옵셔널 체이닝) : 객체의 속성 또는 메서드에 접근할 때 객체가 null, undefined인 경우에도 연산을 중단하고 undefined 반환
- ??
- delete
- new  :  생성자 함수를 호출하여 객체를 생성, 반환
- instanceof : 객체가 함수의 인스턴스인지 확인. 인스턴스면 true, 아니면 false
- in
```

# js 8장

````txt
제어문 : 조건문이나 반복문을 작성할 때 사용 / 조건에 따라서 코드 진행 방향이 결정됨

고차함수 : 함수의 매개변수로 함수를 전달(함수에 함수를 정의)

ex) window.addEventListener(문자열타입, 함수타입)

**블록문**

0개 이상의 명령문을 중괄호로 묶은 것, 코드 블록 또는 블록이라 부름

ex) { var gogo = 10; }

**조건문**

조건식에 따라 코드 블록의 실행이 결정

조건문으로 if와 switch 있음. 주로 if문 우선 사용

리액트에서 reducer할 때 switch 접근

- if문
if(조건){
}else if (조건){
}else{   }

ex)
```jsx
if (조건식1){
	// 조건식1이 true(참)인 경우 실행
} else if(조건식2) {
	// 조건식1이 false(거짓)이고,
	// 조건식2이 true(참)인 경우 실행
} else {
	// 조건식1이 false(거짓)이고,
	// 조건식2도 false(거짓)인 경우 실행
}
```

if문의 조건식에서 출력되는 값은 boolean 타입이어야 함

- switch문

switch 문은 조건식의 결과에 일치하는 case 문을 실행

```jsx
switch (조건식) {
  case 결과1:
    // switch 문의 조건식의 결과가 결과1과 일치하면 실행.
    break;
  case 결과2:
    // switch 문의 조건식의 결과가 결과2과 일치하면 실행.
    break;
  default:
  // switch 문의 case 문들과 일치하는 결과값이 아닌 경우 실행.
}
```

**반복문**

for문과 while문이 있는데, 반복 횟수가 명확하다면 for문, 불명확하다면 while문 사용

> **반복을 대체할 수 있는 다양한 기능**

- **forEach 메서드 : 배열을 순회할 때 사용**
  [1,2,3]
- **for in 문 : 객체의 프로퍼티를 열거할 때 사용**
  {
  age: 1,
  marry: false,
  nicName: “Chlie”
  }
- **for of 문 : 이터러블(순서가 있는)을 순회 가능**

- **for문 :** 조건식이 **true인 동안 반복**실행

```jsx
for (변수 선언문 또는 할당문; (조건식); 증감식){
	// 조건식이 참인 경우 반복 실행될 코드;
}
```

- while문 : 조건식이 true면 코드를 반복하여 실행

```jsx
while (조건식) {
  // 실행 코드
}
```

**break 문**

break 문은 switch 문과 while 문에서 코드 블럭을 **탈출** 할 때(**멈출 때**) 사용

레이블 문, 반복문, switch 문 이외에서 break 문을 사용하면 SyntaxError(문법 에러)가 발생

```jsx
// 문자열에서 특정 문자의 인덱스 검색하기
var string = "Hello World.";
var search = "l";
var index;

for (var i = 0; i < string.length; i++) {
  // 문자열의 개별 문자가 "l"이면
  if (string[i] === search) {
    index = i;
    break; // 반복문을 탈출한다.
  }
}
//console.log(index); // 2
document.write(index); // 2
```

**continue문** : 반복문의 코드 블록 실행을 현 지점에서 중단하고 반복문의 증감식으로 실행 흐름을 이동

````

# js 9장

```txt
타입 변환 : 데이터를 한 타입에서 다른 타입으로 변환하는 프로세스

명시적 타입 변환 : 개발자가 타입을 강제 변환 // 타입 캐스팅

암묵적 타입 변환 : JS가 타입을 자동으로 변환 // 타입 강제 변환

- 개발자가 결과를 예측할 수 있어야 함(대비책)
- 코드 에러가 아니고 원하는 결과가 아닌 경우
- + 연산자
’글자’ + ‘글자’ = ‘글자’
숫자 + 숫자 = 숫자
’글자’ + 숫자 = ‘글자’
- - 연산자
’글자’ + ’글자’ = NaN
숫자 - 숫자 = 숫자
’ 글자 ‘ - 숫자 = ‘글자’

**암묵적 타입 변환**

- 불리언 타입으로 변환

**Boolean Falsy한 것들을 반드시 알아야함**

**: false, undefined, null, 0, NaN, ‘’**

jsx
if ('')     console.log('1');
if (true)   console.log('2');
if (0)      console.log('3');
if ('str')  console.log('4');
if (null)   console.log('5');

// 2 4


**명시적 타입 변환**

문자열 데이터 지정 만들기

변수 + ‘ ’

숫자 데이터 지정 만들기

**parseInt(변수) : 정수 만들기**

parseFloat(변수) : 실수 만들기

## 단축평가

: 논리 연산자를 사용한 단축평가. 표현식의 평가 결과가 확정된 경우 더 이상 평가를 진행하지 않음

- 논리곱(&&)
  두 피연산자가 모두 true로 평가될 때 true 반환.
  ”비욘세” && “디카프리오” = “디카프리오”
  : 비욘세가 문자열인 true이기 때문에 디카프리오가 평가 결과를 결정함
  논리 연산의 결과를 결정하는 두 번째 피연산자를 그대로 반환
- 논리합(||)
  첫 피연산자가 true로 평가되면 전체식을 참으로 결정
  ex) const category = params.category || “all” ;
- params.category가 falsy하지 않으면 params.category를 category에 담고, falsy하면 “all”을 담음

### 옵셔널체이닝이 나오게 된 이유

: Synatax 에러로 js가 멈추지 않게 하기 위해 / 객체의 속성에 접근할 때 객체가 flasy할 수 있는 상황을 고려하여 안전하게 접근

ex)

var elem : null
var result = elem ? elem.gogo : undefined;
var result = elem **?.** gogo

병합 연산자 (??)

const result = null ?? “없군요” ⇒ 결과값 “없군요”

const result = “안녕” ?? “없군요” ⇒ 결과값 “안녕”

```

# js 10장

```txt
- 너무 중요해요.
   : 활용빈도 말도 안되게 높고,
   : 본인 및 타소스를 이해하려면 알아야 해요.
   : 핵심은 JS 의 모든 자료타입은 객체입니다.

   - 타입(js가 리터럴로 인정하는 자료의 종류)

   : 원시 타입
    ( string, number, null, undefined, bool, symbol )

   : 객체타입
     ( [ 원시타입들... ] ,  { 속성명:원시타입 }, function ....  )


   - 객체 구성 ( 객체가 가진 데이터를 객체 내에서 제어하겠다.)

   : 객체에 포함된 변수를 `프로퍼티/속성` 이라고 호칭
   : 객체에 포함된 함수를 `메소드/기능` 이라고 호칭
      const obj = {

        "프로퍼티명" : 원시값 또는 다른 객체,
        "프로퍼티명" : string,
        "프로퍼티명" : [],
        "프로퍼티명" : {},
        "메소드명" : function () {},
      }

    - 객체 만드는 법
       인스턴스 란 ?
          : 남에게 말해주기가 어려운 개념
          : `객체를 생성하는 방법을 활용` 해 생성한 변수를 인스턴스라고 한다.

     1. 객체 리터럴 문법 : 활용빈도 높다. const 인스턴스 = {}

     const  인스턴스 = {
         "myName"  : 5,
          myJob     : 5,
         "my-age"   : 5,
         say   : function () { this["my-age"]  },
         sayHi : () => { this["my-age"]  },
     }
     인스턴스.myName
     인스턴스["myJob"]
     인스턴스.say()
     인스턴스["say"]()
     인스턴스.gogo = "안녕"

      : 객체 리터럴 문법 보완 및 축약 (ES6)

        // 기본형
        const 인스턴스변수 = {
          프로퍼티명: 프로퍼티값 ,
          프로퍼티명: 프로퍼티값 ,
          메소드명 : function() { },
          메소드명 : function() { }
        };

        const age = 10;
        const nickName = "홍길동";

        // 외부 변수 전달 받는데    이름이 똑~~ 같다?
        const person = {
           age      : age,
           nickName : nickName
        };

        //  축약형
        const person = {age, nickName};

        // 메소드 기본형
        const person = {
           say      : function() { }
        };

        // 메소드 축약형
        const person = {
           say() { }
        };



     2. Object 함수 문법

     3. 생성자 함수 문법 : 활용빈도 높다.

     4. Object.create 함수 문법

     5. class 함수 문법 : 활용빈도 높다.
```

# js Syntax 코드 위치

1. inline 방식

```html
<div class="wrap" onclick="alert('안녕');"></div>
```

2. 태그 방식

```html
<script>
  alert("반가워");
</script>
```

3. 외부파일 방식

```html
<script src="./js/script.js">
  alert("반가워"); // 실행안됨
</script>
```

# Swiper Slide 적용해 보기

- Slide 를 직접 코딩하지 마세요.
- 사용법을 배운다.
- Swiper(https://swiperjs.com/), Slick(https://kenwheeler.github.io/slick/), BxSlider(https://bxslider.com/) 가 있어요.

## 1. Swiper 슬라이드 적용시 주의 사항

- html 로드 완료 및 이미지 로드 완료 후 실행 권장.

```js
window.addEventListener("load", function () {
  // 실제 슬라이드 코드 배치하자.
});
```

# Swiper Slide 적용해 보기 2.

- 데모사이트의 core 메뉴를 통해서 참조한다.
- 기본 css 와 js 파일은 CDN 으로 참조한다.

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css"
/>
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
```

- 기본형 코드를 작성해서 원하는 영역에 배치한다.
- 슬라이드 개수 만큼 swiper-slide div 를 만든다.

```html
<div class="swiper 원하는이름">
  <div class="swiper-wrapper">
    <div class="swiper-slide">내용</div>
    <div class="swiper-slide">내용</div>
    <div class="swiper-slide">내용</div>
  </div>
</div>
```

- css 로 `원하는이름` 을 찾아서 width, height 를 100% 주자.
- css 로 `원하는이름` 에 절대로 display 등을 넣으면 안되요.

# Swiper Slide 적용해 보기 3.

- 외부 데이터 연동(json)
- 데이터의 구조를 설계
- json 이란 javaScript Object Notation 입니다.

```json
[
  { "키": 값, "키": 값, "키": 값 },
  { "id": 2, "pic": "b2.png", "url": "#" },
  { "id": 3, "pic": "b3.png", "url": "#" },
  { "id": 4, "pic": "b4.png", "url": "#" }
]
```

# Swiper Slide 적용해 보기 4.

- 비동기 호출하기(vanila/pure js)
  : BE 와 협업시 활용합니다.
- fetch 를 활용 가능
- async await 활용 가능

# Swiper Slide 적용해 보기 5.

- 외부 js 파일을 이용한다.

```html
<script src="./js/파일명.js"></script>
```

```js
window.addEventListener("load", function () {
  //내용작성;
});
```

- swiper 에 보여줄 데이터를 외부 .json 파일로 연동한다.
  : 자료(데이터)를 만들어주는 동료가 BackEnd 입니다.
  : BE 와 협의가 필요하다. (협업의 기본)
  : 초기에는 가짜데이터(Dummy, Mockup) 을 가지고 작업

```json
[
  { "키명": "키값" },
  { "키명": "문자열" },
  { "키명": 55},
  { "키명": true},
  { "키명": []}
  { "키명": {} }
]
```

```json
[
  {
    "id": 1,
    "pic": "b1.png",
    "url": "#",
    "title": "AI 헬스케어의 <br/> 마일스톤을 찍다"
  },
  {
    "id": 2,
    "pic": "b2.png",
    "url": "#",
    "title": "카카오브레인의 <br/> 연구문화"
  },
  {
    "id": 3,
    "pic": "b3.png",
    "url": "#",
    "title": "PathFinder 2기의 <br/> 언어모델 활용기"
  },
  {
    "id": 4,
    "pic": "b4.png",
    "url": "#",
    "title": "칼로리의 꿈 <br/> 시리즈 ③"
  }
]
```

- json 데이터를 이용해서 자료를 추출한다.
  : 외부 주소를 통해서 자료를 불러들이기 위해 fetch 를 알고 적용한다.
  : 더불어서 크롬 개발자 도구 (F12) 의 NetWork 탭을 알아야 한다.
  : 옵션으로 Fetch/XHR 을 선택할 수 있어야 한다.
  : request 와 response 를 구별하여 파악할 수 있어야 한다.

```js
fetch("주소").then().then().catch();
```

```js
fetch("주소")
  .then((결과) => {
    const 접속결과 = 결과.json();
    return 접속결과;
  })
  .then()
  .catch();
```

```js
fetch("주소")
  .then((결과) => {
    const 접속결과 = 결과.json();
    return 접속결과;
  })
  .then(function (최종자료) {
    // 하고 싶은 일 마음대로....
  })
  .catch();
```

```js
fetch("주소")
  .then((결과) => {
    return 접속결과;
  })
  .then((최종자료) => {
    // 하고 싶은 일 마음대로....
    // 우리가 할 일을 진행
  })
  .catch((오류) => {
    // 오류처리
  });
```

- 추출된 데이터로 html 을 생성한다.
  : 백틱(``)을 적극적으로 사용

```js
const test = `<div class="swiper-slide">
          <a href="${data.url}" style="background :url('./images/${data.pic}') no-repeat center; background-size: cover;">
            <p class="slide-title">
              ${data.title}
              연구문화
            </p>
          </a>
        </div>`;
slideTags += test;
```

: html을 작동

```js
// 원하는 장소에 출력해 보기
const whereTag = document.querySelector(".topslide .swiper-wrapper");
whereTag.innerHTML = slideTags;
```

- swiper 를 작동시킨다.
  : html 완료 후 슬라이드 생성

```js
// DOM 을 다루려고 하는 목적인 경우
window.addEventListener("load", function () {
  // 1. 외부에서 자료를 불러온다.
  const dataUrl = "./apis/topslide.json";

  fetch(dataUrl)
    .then((response) => {
      // Step 1. 자료 받아서 json 변경하기
      // 토큰을 js의 데이터로 변경하기
      const data = response.json();
      // 변환된 결과를 돌려주기
      return data;
    })
    .then((result) => {
      // Step 2. json 변경된 데이터 활용하기
      // 전체 글자 모음
      let slideTags = "";
      for (let i = 0; i < result.length; i++) {
        const data = result[i];
        // 템플릿 문법 필요(백틱 / html 생성)
        const test = `<div class="swiper-slide">
          <a href="${data.url}" style="background :url('./images/${data.pic}') no-repeat center; background-size: cover;">
            <p class="slide-title">
              ${data.title}
              연구문화
            </p>
          </a>
        </div>`;
        slideTags += test;
      }
      // 2. 자료를 이용해서 슬라이드에 배치할 html 을 만든다.
      // 원하는 장소에 출력해 보기
      const whereTag = document.querySelector(".topslide .swiper-wrapper");
      whereTag.innerHTML = slideTags;

      // 3. html 완성후 swiper 를 생성한다.
      // 기본코드를 넣어보자.
      var topSlide = new Swiper(".topslide", {});
    })
    .catch((error) => {
      console.log(error);
    });
});
```

# Swiper Slide 적용해 보기 6.

- 옵션(https://swiperjs.com/demos#autoplay)
  : loop
  : autoplay
  : effect
  : speed
  : pagenation(https://swiperjs.com/demos#pagination)
  : 페이지네이션 디자인 수정하기 참조

```css
.bannerslide .swiper-pagination {
  bottom: 30px !important;
}
.bannerslide .swiper-pagination-bullet {
  width: 4px !important;
  height: 4px !important;
  background: #ffffff !important;
  opacity: 0.7 !important;
  border-radius: 4px !important;
  transition: width 0.3s;
  margin: 0 2px !important;
}
.bannerslide .swiper-pagination-bullet-active {
  background: #ffffff !important;
  opacity: 1 !important;
  width: 20px !important;
}
```

# css의 opcity와 position의 이해

- opacity는 DOM의 내용까지도 투명도가 적용됨
- position
  : position 중 absolute로 픽셀 위치 설정의 경우 반드시 바깥 영역에도 position 코드가 있어야 함
  : position 중 fixed는 웹 브라우저를 기준으로 배치
  : fixed는 반드시 left, top, right, bottom을 주자
  : fixed는 보통 z-index를 준다
  : fixed는 높이에 반영이 안되므로 주의(레이아웃 배치 문제)

```css
대상 {
  position: relative;
}
대상 {
  position: absolute;
}
대상 {
  position: fixed;
}
```

- 주의사항

```css
.box-wrap {
  position: relative;
  margin: 0 auto;
  width: 600px;
  height: 300px;
  background: orange;
}
.box {
  position: absolute;
  /* absolute 상위에 position 있어야함 */
  right: 80px;
  bottom: 20px;

  width: 200px;
  height: 200px;
  background: red;
}
```

# js 윈도우 스크롤의 위치를 알아내기

```js
window.addEventLinstenr("scroll", function () {
  // 하고 싶은 일
});
```

```js
window.addEventLinstenr("scroll", function () {
  // 스크롤바의 위치
  const scY = window.scrollY;
});
```

# js로 css의 클래스 동적으로 활용하기

```js
// DOM 찾아서 변수로 레퍼런스 하기
const tags = document.querySelector(".클래스명");
// DOM을 이용해서 선택한 곳에 적용된 css 클래스 목록 추가
tags.classList.add("클래스명");
// DOM을 이용해서 선택한 곳에 적용된 css 클래스 목록 제거
tags.classList.remove("클래스명");
// DOM을 이용해서 선택한 곳에 적용된 css 클래스 목록 추가 / 제거
tags.classList.toggle("클래스명");
// DOM을 이용해서 선택한 곳에 적용된 css 클래스 목록 포함여부
tags.classList.contain("클래스명");
```

# js의 함수란 1번

```js
// 함수 만들기
function 적절한동사() {
  // 하고 싶은 일 작성 ...
}
// 함수 사용하기(함수호출)
적절한동사();
// 예시
fetch().then().then().catch();
```

- 함수는 무조건 1개의 값을 리턴하도록 규정되어 있음
- 리턴 : 함수 실행 후 값을 돌려주는 것을 말함

```js
function 함수명() {
  // 몰래 작성됨 return undefined;
}
함수명();
```

- 함수 정의 문

```js
function 함수이름() {
  // 할일
}
```

- 함수 실행/호출(call)문

```js
함수이름();
```

# js 함수의 매개변수란? 2번

- 초기 기능 즉, 함수를 정의하기 전 기능 상 자주 변하는 데이터를 고민
- 기능은 스크롤시 특정 위치보다 커지면 css 추가
- 함수는 스스로 지역 즉, Local 영역(Scope)에서 처리되는 것이 좋다고 봄
- `처리` : 변수를 찾거나 잘못된 값이 전달되어 오류가 나는 것 방지

```js
function sum() {
  return 5 + 6;
}

const a = 5;
const b = 0;
function divide(_num1, _num2) {
  if (b === 0) {
    alert("나눗셈에서 0은 안됨");
  }
  return a / b;
}
divide(a, b);
```

# 함수의 이해 3번

1. 함수를 만들어야겠다고 판단하는 케이스

- 동일한 코드가 2번 이상 반복되면 함수를 만드려고 하자
- 반복이 되지 않더라도 하나의 기닝이 너무 복잡하면 함수를 만들려고 하자
- 복잡하지 않은데 코드가 너무 길어지면 함수로 묶어주려고 하자
- 실행의 결과가 그때, 그때 다른 경우에도 만들자

2. 화살표 함수를 만들어야 하는 이유

- 트랜드 쫒아가기
- this를 정확히 지정하기 위해서
- 코드가 해석하기 더 어려워지기 때문에

```js
function say() {
  console.log("안녕", this);
}
```

: step 1.

```js
say()=>{
  console.log("안녕", this);
}
```

: step 2.

```js
const say = () => {
  console.log("안녕", this);
};
```

: 매개 변수가 있는 경우

```js
function say(_who) {
  console.log("안녕", _who, this);
}
```

: step 1.

```js
say(_who)=>{
  console.log("안녕", _who, this);
}
```

: step 2.

```js
const say = (_who) => {
  console.log("안녕", _who, this);
};
```

- this의 정확한 이해
  : 화살표 함수를 사용하면 일반적으로 큰 고민없이 사용
  : but, 함수 안에 this를 작성하면 상황이 달라짐
  : 화살표 함수에서 this는 window를 가르킴
  : 결론은 화살표 함수에서 this를 사용한다면 console.log(this) 확인 필수
  : 화살표 함수는 예전 일반 함수에서 window를 참조하지 못하는 문제를 해결

```js
// this 의 차이
const btWrap = document.querySelector(".bt-wrap");
// 일반 함수는 this가 타이핑이 된 곳을 가르킨다
btWrap.addEventListener("click", function () {
  console.log(this);
});
// 화살표 함수는 this가 window를 가르킨다
btWrap.addEventListener("click", () => {
  console.log(this);
}); // 따라서 화살표 함수에서 this 사용 주의
```

# 배열의 이해

- [ 요소, 요소, 요소, 요소]
  : 요소로 담을 수 있는 자료형은 7가지
- 배열의 속성(배열을 위한 특별한 변수)은 1개가 있음
  : length (요소의 개수)
- 배열의 메소드(배열을 위한 특별한 함수)는 매우 많음
- 상당히 많은 메소드(배열을 위한 함수)가 있음
- 배열.forEach((요소)=>{}), 배열.map((요소)=>{}), 배열.filter((요소)=>{}), 배열.find((요소)=>{})

```js
// 배열이라면 반복하자.
result.forEach((item) => {
  const tag = `<a href=${item.link} class="list-box">
        <div class="list-box-img br-20" style="background: url('./images/${item.imgpath}') no-repeat center; background-size: cover"></div>
        <div class="list-box-cate">
          <img src="./images/icon/${item.icon}" alt="${item.category}" />
          <span style="color:${item.txtcolor};">${item.category}</span>
        </div>
        <p class="list-box-title">${item.title}</p>
        <span class="list-box-day">${item.day}</span>
        </a>`;
  allTag = allTag + tag;
});
```

# 카카오 브레인 블로그 사이트

- 저작권 밝히기
- 첫 화면만 연습하면 된다
