# css header 영역

## 1. html 태그 작업

### 1.1. anchor 태그

- `<a href="보여줄 페이지 주소"> 글자 </a>`
- `<a href="보여줄 페이지 주소"> 그림 </a>`
- `<a href="보여줄 페이지 주소" target="_blank"> 네이버 </a>`
  : 새 탭으로 보여주기(`target="_blank"`)

### 1.2. img 태그

- 파일명.jpg, 파일명.png, 파일명.gif, 파일명.svg
- tip 1. 1순위 .png
- tip 2. FE는 .WebP (Next.js 기본)
- 상식. gif는 여러장의 이미지를 일정한 시간으로 교체하면서 보여주는 파일

- `<img src="경로/파일명.확장자" />`
- `<img src="경로/파일명.확장자" alt="이미지설명" />`

### 1.3. 목록태그(`ul, li`)

- 필수임
- 판단할 때 레이아웃이면 `div`, 내용이 동일한 형태면 `ul, li`

## 2. css 선택자

### 2.1. 범위 안쪽에 있는 태그 찾기

```css
.header-logo-slide img {
  ....;
}
.header-logo-slide a {
  ....;
}
```

### 2.2. display 간단 이해

- 신규 프로젝트는 적극적으로 `display:flex` 활용
- 유지, 보수 프로젝트는 `display:inline, display:inline-blodck`을 조심

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>레이아웃</title>
    <style>
      div,
      header,
      footer {
        border: 5px solid red;
      }

      main {
        display: none;
      }

      .community {
        display: flex;
      }
      .news {
        display: block;
        width: 25%;
        height: 400px;
      }
      .notice {
        display: block;
        width: 25%;
        height: 400px;
      }
      .banner {
        display: block;
        width: 25%;
        height: 400px;
      }
      .product {
        display: block;
        width: 25%;
        height: 400px;
      }
    </style>
  </head>
  <body>
    <!-- 전체 레이아웃 -->
    <div class="wrap">
      <!-- 상단 -->
      <header class="header">상단</header>
      <!-- 메인 -->
      <main class="main">
        <div class="slide">슬라이드</div>
        <div class="community">
          <div class="news">뉴스</div>
          <div class="notice">공지사항</div>
          <div class="banner">배너</div>
          <div class="product">제품소개</div>
        </div>
      </main>
      <!-- 하단 -->
      <footer class="footer">하단</footer>
    </div>
  </body>
</html>
```

### 2.3. flex 기초

- 관련 사이트

  - https://codepen.io/enxaneta/pen/adLPwv
  - https://studiomeal.com/archives/197
  - https://flexboxfroggy.com/#ko

- container 용 flex(상자)

```css
.header-logo-link {
  display: flex;
  /* 세로 중앙 */
  align-items: center;
  /* 가로 왼쪽 정렬 */
  justfy-content: flex-start;
  /* 가로 가운데 정렬 */
  justfy-content: center;
  /* 가운데 우측 정렬 */
  justfy-content: flex-end;
  /* 가운데 양쪽 균등 정렬 */
  justfy-content: space-between;
  justfy-content: space-around;
  /* 아이템과 아이템 사이의 여백 */
  gap: 30px;
}
```

- item 용 flex(요소들)

### 2.4 글꼴

- 초기 디자인 및 css 작업은 글꼴에 대한 협의가 끝나고 진행한다. (1순위)
- [구글폰트](https://fonts.google.com/?query=inter) 검색 > [눈누](https://noonnu.cc/) 검색
- 존재하지 않는 경우 직접 폰트생성 진행
