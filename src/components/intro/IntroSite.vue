<template>
  <div className="intro__items bg-blue nexon5">
    <h2>내가 만든 사이트 모음</h2>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        <a :href="item.url" target="_blank" rel="noreferrer">
          <img :src="`./images/introPage/${item.src}`" :alt="item.title" />
          <span>{{ item.title }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          url: "https://kebab000.github.io/web2023/",
          src: "introitem00.png",
          title: "webs2023 메인페이지",
        },
        {
          url: "https://kebab000.github.io/web2023/class/index.html",
          src: "introitem01.png",
          title: "클라스 페이지",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/index.html",
          src: "introitem02.png",
          title: "자바스크립트 정리 메인페이지",
        },
        {
          url: "https://kebab000.github.io/web2023/w-webd/index.html",
          src: "introitem03.png",
          title: "레이아웃 모형 페이지",
        },
        {
          url: "https://kebab000.github.io/web2023/site/index.html",
          src: "introitem04.png",
          title: "사이트 만들기",
        },
        {
          url: "https://kebab000.github.io/web2023/site/site1/index.html",
          src: "introitem05.png",
          title: "사이트 완성01",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/parallax/parallaxEffectAA.html",
          src: "introitem06.png",
          title: "페럴랙스 이펙트",
        },
        {
          url: "http://kebab00.dothome.co.kr/php/index.html",
          src: "introitem07.png",
          title: "PHP블로그",
        },
        {
          url: "http://kebab00.dothome.co.kr/php2/index.html",
          src: "introitem08.png",
          title: "PHP팀프로젝트",
        },
        {
          url: "https://kebab000.github.io/web2023/mysql/index.html",
          src: "introitem09.png",
          title: "MYSQL 설명",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/quiz/quizEffect01.html",
          src: "introitem10.png",
          title: "퀴즈 이펙트01",
        },
        {
          url: "https://kebab-sgame.web.app/",
          src: "introitem11.png",
          title: "게임이펙트",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/mouse/mouseEffect01.html",
          src: "introitem12.png",
          title: "마우스 이펙트01",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/search/searchEffect01.html",
          src: "introitem13.png",
          title: "검색 이펙트01",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/parallax/parallaxEffect01.html",
          src: "introitem14.png",
          title: "패럴랙스 이펙트01",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/slider/sliderEffect01.html",
          src: "introitem15.png",
          title: "슬라이드 이펙트01",
        },
        {
          url: "https://kebab000.github.io/web2023/javascript/portfolio/ex1/index.html",
          src: "introitem16.png",
          title: "포트폴리오 이펙트01",
        },
      ],
    };
  },
};
</script>
<styel lang="scss">
// intro item
.intro__items {
  padding: 30px;
  h2 {
    font-size: 50px;
    text-align: center;
    margin-bottom: 30px;
  }
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 24%;
      margin-bottom: 4%;

      img {
        width: 100%;
        object-fit: cover;
        height: 200px;
      }
      span {
        display: block;
        margin: 4px 0;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        -webkit-line-clamp: 1; /* 라인수 */
      }
    }
  }
}
</styel>
