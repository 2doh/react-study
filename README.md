# js 14장

```txt
  // var : 값을 담을 공간을 마련해줘.....
  // var 이름 : 값을 담은 공간에 꼬리표를 붙여줘.
  var age = 15;
  var nickName = "hong";
  function go(){
  }
  console.log(age)
  console.log(window.age)

  모듈(기능별 파일코드)은 import/export 문법을 써서 변수 범위를 설정한다.

 class 장을 보아야 해요.

  외부에서 변수 및 함수에 접근할 수 있는 권한
  public    : 외부 어떤 곳에서도 사용할 수 있다.
  private   : 외부에서 절대로 사용할 수 없다.
  protected : 허용한 대상만 사용할 수 있다.
```

# js 15장

```txt
동일한 이름의 변수가 이미 선언되어 있는 것을 모르고 변수를 중복 선언하고 값까지 할당했다면 의도치 않게 먼저 선언된 변수 값이 변경되는 부작용이 발생

var 키워드로 선언한 변수는 오로지 **함수의 코드 블록** 만을 지역 스코프로 인정한다. 따라서 함수 외부에서 var 키워드로 선언한 변수는 코드 블록 내에서 선언해도 모두 전역 변수가 된다.

const 변수이름 : 값을 고정시키겠다
let 변수이름 : 값이 수시로 바뀌어진다

const 객체 = {}   :   오해의 소지 발생  // const로 선언한 변수는 재할당이 되지 않으나, 객체는 재할당이 가능함

if.
const 정군 = {}     // 이미 주소는 고정이 됨
정군 = “안녕”       //  주소를 교체하려고 했으므로 const에 위배, 에러

정군.age = 100;         //   주소가 아닌 안쪽의 내용을 수정, O
정군[”nickName”] = “hong guil dong”;      //   주소가 아닌 안쪽의 내용을 수정, O
```

# 실 업무에서 알아야 하는 상식

- nvm (Node Version Manager) 설치 및 활용
  : https://github.com/coreybutler/nvm-windows/releases
  : 설치 버전 확인 `nvm -v`
  : 설치 가능한 버전 목록 `nvm list available`
  : 설치 하기 `nvm install 버전`
  : 현재 사용중인 Node 버전 확인하기 `node -v`
  : 현재 설치된 Node 목록 확인 `nvm ls`
  : 사용할 Node 버전 선택하기 `nvm use 18.17.1`
  : Node 설치된 경로 알아보기 `which node`
  : Node 버전 삭제 `nvm uninstall 18.17.1`
- npm 보단 yarn 선호
  : Node Package Manager (node_modules)
  : package.json 의 dependency 목록을 참조
  : npm이 가끔 다운로드 중 오류가 발생하고, 소스 깨짐 현상
  : ex. 네이버 Toast UI 등
  : npm 보다 안정적인 package 관리를 위해서 yarn을 활용함
  : `npm install -g yarn`
  : `yarn --version`
- favicon 만들기 (보통 디자이너 담당)
  : https://realfavicongenerator.net/

# React 기초 2 리액트 컴포넌트

## 1.0. 컴포넌트를 왜 생성하는가

- 프로젝트 규모에 따라 협업이 필요 함
- 기능별로 html, css, js가 별도로 관리 필요

## 1.1. 컴포넌트에 배치되는 내용

- 컴포넌트 : html을 묶어준 것
- 하나의 화면은 여러개의 요소(컴포넌트)를 배치해서 보여준다

- JSX가 배치된다(리액트용 HTML 태그 / class => className)
<!--
- pages 폴더 : 화면을 보여주는 것들
- components 폴더 : page를 구성하는 요소들 (ex. Header.js)

HTML : 2가지 분리해서 호칭

- 퍼블리싱 html
- JSX Element -->

- css가 배치된다(background : url(경로 문제))
- js가 배치된다

## 1.2 이미지를 배치하는 2가지 경우(주의사항)

- 태그에 이미지를 배치한 경우
  : public/images 폴더를 참조함.

```html
<img src="./images/etc/logo-kakao.png" />
```

- css 배경으로 이미지를 배치한 경우
  : src/images 폴더를 참조
  : css파일을 js 컴포넌트에서 사용하면 webpack이 압축한다

```css
background: url("../images/icon/icon-search.png");
```

## 1.3 js를 React로 마이그레이션 진행

### 1.3.1. load가 useEffect로 변경

```js
window.addEventListener("load", function () {});

useEffect(() => {
  return () => {};
}, []);
```

### 1.3.2. querySelector가 useRef(null)로 변경

```js
const tag = document.querySelector(".bt");

const tag = useRef(null);

useEffect(() => {
  // tag.current 로 접근
  return () => {};
}, []);

<div ref={tag}> </div>;
```
