<template>
  <div class="port__slider nexon5">
    <swiper
      :modules="modules"
      :slides-per-view="3.5"
      :spaceBetween="3"
      :pagination="{ clickable: true }"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :autoplay="{ delay: 0 }"
      :speed="6000"
    >
      <swiper-slide v-for="(port, index) in ports" :key="index">
        <a :href="port.url" target="_blank" rel="noreferrer">
          <img :src="`./images/port/${port.portImg}`" :alt="port.name" />
          <h4>{{ port.name }}</h4>
        </a>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// import Swiper core and required modules
import { Navigation, Pagination, Autoplay } from "swiper";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation, Pagination, Autoplay],
    };
  },
  data() {
    return {
      ports: [
        {
          name: "이요셉",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port00.png",
          url: "https://kebab-portfolio.web.app/",
          profileImg: "member106.svg",
        },
        {
          name: "진현미",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port01.png",
          url: "https://portfolio-hyunmi.netlify.app/",
          profileImg: "member80.svg",
        },
        {
          name: "천설희",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port05.png",
          url: "https://portfolio-313.web.app/",
          profileImg: "member05.svg",
        },
        {
          name: "장진용",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port02.png",
          url: "https://portfolio-cc509.web.app/",
          profileImg: "member02.svg",
        },
        {
          name: "김도현",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port03.png",
          url: "https://kdh-portfolio.netlify.app",
          profileImg: "member03.svg",
        },
        {
          name: "이양구",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port04.png",
          url: "https://leeyanggoo-portfolio.web.app/",
          profileImg: "member04.svg",
        },
        {
          name: "이승연",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port06.png",
          url: "https://dkdlelw-portfolio.web.app/",
          profileImg: "member06.svg",
        },
        {
          name: "김현빈",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port07.png",
          url: "https://portfolio-hyenobeen.netlify.app/",
          profileImg: "member07.svg",
        },
        {
          name: "정황우",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port08.png",
          url: "https://jhwportfolio.netlify.app/",
          profileImg: "member08.svg",
        },
        {
          name: "여다슬",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port09.png",
          url: "https://yds-portfo.web.app/",
          profileImg: "member09.svg",
        },
        {
          name: "이은지",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port10.png",
          url: "https://my-portfolio-vite.web.app/",
          profileImg: "member10.svg",
        },
        {
          name: "노지영",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port11.png",
          url: "https://noji-portfolio.netlify.app/",
          profileImg: "member11.svg",
        },
        {
          name: "이훈규",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port12.png",
          url: "https://hoongportfolio.netlify.app/",
          profileImg: "member107.svg",
        },
        {
          name: "신동진",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port13.png",
          url: "https://sdj-portfolio-5a461.web.app/",
          profileImg: "member13.svg",
        },
        {
          name: "김도현",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port15.png",
          url: "https://portfolio-45429.web.app/",
          profileImg: "member15.svg",
        },
        {
          name: "변우현",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port16.png",
          url: "https://fitalux-portfolio-vite-2023.netlify.app/",
          profileImg: "member16.svg",
        },
        {
          name: "안교남",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port17.png",
          url: "https://portfolio-18b72.web.app/",
          profileImg: "member17.svg",
        },
        {
          name: "전윤기",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port18.png",
          url: "https://myportpolio-e7f37.web.app",
          profileImg: "member18.svg",
        },
        {
          name: "권현정",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port19.png",
          url: "#",
          profileImg: "member19.svg",
        },
        {
          name: "정희석",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port20.png",
          url: "https://getgrovy-port.web.app/",
          profileImg: "member20.svg",
        },
        {
          name: "이유나",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port21.png",
          url: "https://yuna-portfolio.web.app/",
          profileImg: "member21.svg",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.port__slider {
  height: 250px;
  margin-bottom: 70px;
  .swiper-wrapper {
    transition-timing-function: linear;
  }
  .swiper-slide {
    overflow: hidden;
    position: relative;
    img {
      height: 250px;
      width: 600px;
      object-fit: cover;
      // &:hover {
      //     scale: 1.3;
      // }
      // transition: all 0.6s;
    }
    h4 {
      position: absolute;
      bottom: 10px;
      left: 30px;
      color: #fff;
      background-color: #292929a6;
      padding: 5px 10px;
      border-radius: 3px;
    }
  }
}
</style>
