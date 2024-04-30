# js 11장

```txt
일반 변수는 값이 보관되고    값이 복사된다.

    객체 변수는 주소가 보관되고 주소가 복사된다.
    : 중요한 것은 객체를 복사하는 것은 주의하자. (얕은복사)
    : 가능하면 객체는 깊은 복사를 활용하도록 노력하자.

```

# js 12장

```txt
원시 데이터 :                                                        => 단일 값
복합 데이터 : 복잡한 속성, 메서드를 가진 객체 => function, [ ], { }
함수는 객체의 문법을 따르는 값이다

function 함수이름 (매개변수){
    return 문장을 작성(값을 반드시 출력 : 표현식)
}

함수이름(인자)                 :    함수 호출

리터럴은 JS가 알아먹을 수 있는 데이터 형태로 작성한 것
ex) const a = 1;                             //  숫자 리터럴
       const add = function( ) { };  //  함수 리터럴

JS의 일급객체에 대해서 설명하라
1. 값처럼 변수에 할당할 수 있는가
  const add = function( ) { }
2. 객체의 프로퍼티의 값으로 담을 수 있는가
  const obj = { add : function( ) { } }
3. 배열의 값으로 담을 수 있는가
  const arr = [ 1, 2, 3, 4, function( ) { }, { }, [ ] ]
4. 함수의 매개변수 값으로 전달할 수 있는가
  function 말해봐(기능){
        기능();
}
  const 안녕 = function( ) {
        console.log("안녕하세요")
}
말해봐(안녕)

말해봐( function( ){ console.log("반가워요") } )



함수가 객체를 생성하는 함수를 객체 생성자 함수.

JS의 함수에 전달되는 매개변수 목록을 arguments 라는 객체 라고 한다
초과되는 매개변수들은 arguments에 담긴다


- 함수의 매개변수로

1. 원시 값을 인자로 전달하는 경우

     const age = 15;
     function grow( _value ) {
         return _value + 5;
     }

     grow(age);

     age 는 변화가 없다.



2. 객체를 인자로 전달하는 경우
const person = { age : 10 }

function growObject(_who){
     _who.age = 150 ;
}

// 객체의 참조(주소) 값 전달
growObject(person);

// 객체의 상태가 변경이 일어난다


- 중첩 함수

function Outer( ){
    function Inner = ( ) => {
   }
   Inner( );
   return ( JSX 구문 )


- 콜백 함수
window.addEventListener("이벤트글자", function( ){ })
}

- 순수 함수
function add(a, b) {
    return a + b;
}

- 비순수 함수
  const age = 10;
function add(b){
   return age + b;
}
```

# 깃 협업(순서 지킬 것)

````txt
1. 카카오가치같이 팀협업

   - 프로젝트명 소문자( kko )
     : TypeScript 로 프로젝트
     : npx create-react-app ./ --template typescript

   - 팀이 협의하에 기본형을 생성한다.
     :  publish/www 폴더 생성/images, css, js, assets,
     : test.txt 파일생성

   - 팀장 기본형 생성 후 GitHub 에 저장소 생성한다.
     : public 으로 생성
     : remote 를 추가

   - 팀원은 GitHub 주소를 공유 받는다.

   - 팀원은 공유받은 주소에 가서 fork 를 받는다.

   - 팀원은 본인의 주소로 가서 fork 주소를 확인한다.

   - 팀원은 PC 에 본인의 깃 허브 주소를 clone 한다.
      git clone https://github.com/아이디/gokko.git

   - 팀원은 PC 에서 브랜치를 생성한다. !!!!!!
     git branch 아이디

   - 팀원은 PC 에서 브랜치로 이동한다.
      git switch 아이디

   - 리액트 프로젝트라서 js 소스들을 다운로드 및 설치 하셔야 해요
      npm i

   - 팀원은 PC 에서 작업하고
      git add .
      git commit
      git push 아이디

   - 팀원은 GitHub 에서 브랜치 확인 후 pull Request 요청한다.

   - 팀원은 대기한다.

   - 팀장은 pull Request 요청을 처리한다.

   - 팀장은 요청에 대해 처리후 feedback (슬랙) 준다.

   - 팀장이 소스 merge 끝났습니다. sync 받으셔요.

   - 팀원은 본인 깃허브 sync fork 클릭합니다.

   - 팀원은 작업 brach 제거한다.
     : git switch main
     : git branch -D 아이디

   - 팀원은 sync 이후에 소스를 다시 받는다.
     : git fetch
     : git merge origin/main

```txt
````
