# css 최적화

# js Syntax 1장

1. Syntax (구문) : 약속된 문법

2. Interpreter (번역 ) : 갤럭시 AI/웹브라우저

3. 프로그래밍은 요구사항을 분석하고, (개인별로 작성 : 의사코드 )
   Syntax 를 이용해서
   적절한 자료구조 + 적절한 함수를 활용하고,
   흐름을 제어하여 요구사항을 만족 시킨다.

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

- 동일한 코드가 2번 이상 반복되면 함수를 만드려고 하자
- 반복이 되지 않더라도 하나의 기닝이 너무 복잡하면 함수를 만들려고 하자
- 복잡하지 않은데 코드가 너무 길어지면 함수로 묶어주려고 하자
- 실행의 결과가 그때, 그때 다른 경우에도 만들자

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
