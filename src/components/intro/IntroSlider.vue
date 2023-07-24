<template>
  <div className="intro__slider nexon5">
    <Swiper
      :modules="modules"
      :slides-per-view="10"
      :spaceBetween="3"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :autoplay="{ delay: 0 }"
      :speed="4000"
    >
      <swiper-slide v-for="(intro, index) in intros" :key="index">
        <img :src="`./images/introPage/${intro.src}`" :alt="intro.title" />
      </swiper-slide>
    </Swiper>
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
      intros: [
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.intro__slider {
  height: 250px;
  margin-bottom: 70px;
  .swiper-wrapper {
    transition-timing-function: linear;
  }
  .swiper-slide {
    overflow: hidden;
    img {
      height: 250px;
      object-fit: cover;
      &:hover {
        scale: 1.3;
      }
      transition: all 0.6s;
    }
  }
}
</style>
