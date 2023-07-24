## vue.js를 사용한 사이트 만들기

<img src="https://raw.githubusercontent.com/kebab000/site2023-vue/main/src/assets/images/intro/p1.png" />
<br><br>
 
- 이 사이트는 vue를 기반으로 만든 사이트로 6개월간 같이 공부한 사람들의 포트폴리오를 모아두었습니다.
- 또한 fetch를 이용해 다양한API(Youtube API, Unsplash API, Movie API 등등)의 정보를 받아오는 방법과 React Hook을 사용해 상태를 관리하는 방법을 학습하였습니다.
<br><br>

- Live Demo : https://2023portfoliosite-vue.netlify.app/

## 사용 스택 

- Vue.js: Vue.js는 현대적이고 유연한 JavaScript 프레임워크로, 사용자 인터페이스(UI)를 구축하기 위해 사용됩니다. 이 코드에서는 Vue.js를 사용하여 웹 페이지의 컴포넌트 기반 렌더링을 구현하고, 각 컴포넌트를 효율적으로 재사용합니다.
- Vue의 단일 파일 컴포넌트 구조 : Vue에서는 컴포넌트를 단일 파일 컴포넌트(Single-File Components)라는 형태로 구성할 수 있습니다. 이는 HTML, JavaScript, CSS 등의 코드를 한 파일에 모두 작성하는 방식으로, 개발자들이 컴포넌트를 보다 구조적으로 관리할 수 있게 해줍니다.
- Vue 템플릿 : <template> 태그 내에서 Vue 컴포넌트의 템플릿을 작성합니다. 템플릿은 사용자에게 보여지는 UI의 구조와 내용을 정의하는데 사용됩니다.
- Vue Router : <router-view />는 Vue.js의 공식 라우터인 Vue Router를 사용한 것입니다. Vue Router는 클라이언트 사이드 라우팅을 구현하여 SPA(Single Page Application)처럼 동작하도록 해줍니다. <router-view />는 라우터에 의해 매칭된 컴포넌트를 렌더링하는 데 사용됩니다.
- SCSS: style 태그 내에서 사용된 lang="scss" 속성은 해당 스타일이 SCSS(Sass)로 작성되었다는 것을 나타냅니다. SCSS는 CSS의 확장 문법으로, 보다 간결하고 효율적인 스타일 코드를 작성할 수 있도록 해줍니다.
- fetch : JavaScript의 fetch 함수를 사용하여 외부 API에 HTTP 요청을 보냅니다. API를 사용하여 자료들 검색하고 가져옵니다.
- 비동기 처리 : await과 async 키워드를 사용하여 비동기 함수를 구현합니다. 이를 통해 비동기적으로 API 호출을 처리하고, 결과가 도착하면 해당 데이터를 Vue 컴포넌트의 상태에 업데이트합니다.
<br><br>

## 구현 내역

- swiper를 활용한 이미지 슬라이드
- router기능을 활용한 페이지
- 탭 메뉴로 구성된 시대별 유명 작품
- Youtube, Unsplash, Movie 이미지 슬라이드, 검색, 태그 기능 (Youtube API, Unsplash API, TMDB API 사용)
