<template>
  <div className="youtube__slider">
    <swiper
      :modules="modules"
      :slides-per-view="3"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :autoplay="{ delay: 3000 }"
      :spaceBetween="3"
    >
      <SwiperSlide v-for="(youtube, index) in youtubes" :key="index">
        <a
          :href="`https://www.youtube.com/watch?v=${youtube.id.videoId}`"
          target="_blank"
        >
          <img
            :src="youtube.snippet.thumbnails.medium.url"
            :alt="youtube.snippet.title"
          />
        </a>
      </SwiperSlide>
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
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang="scss" scoped>
.youtube__slider {
  overflow: hidden;
  width: 100%;
  a {
    img {
      width: 100%;
      object-fit: cover;
    }
  }
}
</style>
