<template>
  <div>
    <main>
      <SliderSection attr="slider__wrap section nexon5" />
      <IntroSection attr="intro__wrap section bg-blue nexon5" />
      <PortSection attr="ports__wrap section center bg-blue" />
      <YoutubeSection attr="youtube__wrap section nexon5" />
      <UnsplashSection attr="unsplash__wrap section bg-blue nexon5" />
      <MovieSection attr="movie__wrap section nexon5" />
    </main>
  </div>
</template>
<script>
// @ is an alias to /src
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";
export default {
  components: {
    SliderSection,
    IntroSection,
    PortSection,
    YoutubeSection,
    UnsplashSection,
    MovieSection,
  },
};
</script>
