<template>
  <div class="youtube">
    <ContTitle title="youtube" />
    <YoutubeSlider :youtubes="youtubes" />
    <YoutubeSearch @onSearch="search" />
    <YoutubeTag @onSearch="search" />
    <YoutubeCont :youtubes="youtubes" />
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import YoutubeSlider from "@/components/youtube/YoutubeSlider.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import { ref, onMounted } from "vue";

export default {
  components: {
    ContTitle,
    YoutubeSlider,
    YoutubeSearch,
    YoutubeTag,
    YoutubeCont,
  },

  setup() {
    const youtubes = ref([]);

    const search = async (query) => {
      try {
        const response = await fetch(
          `https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=28&q=${query}&type=video&key=AIzaSyDu13VB1Y6cnu4y9DKqA3bLgAXuqaw4BFU`
        );
        const result = await response.json();
        youtubes.value = result.items;
      } catch (error) {
        console.log("error", error);
      }
    };

    onMounted(async () => {
      try {
        const response = await fetch(
          "https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=28&q=%EC%BD%94%EB%94%A9%EC%95%A0%ED%94%8C&type=video&key=AIzaSyDu13VB1Y6cnu4y9DKqA3bLgAXuqaw4BFU"
        );
        const result = await response.json();
        youtubes.value = result.items;
      } catch (error) {
        console.log("error", error);
      }
    });

    return {
      youtubes,
      search,
    };
  },
};
</script>
