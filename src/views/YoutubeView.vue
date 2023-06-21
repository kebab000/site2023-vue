<template>
  <div class="youtube">
    <ContTitle title="youtube" />
    <YoutubeSlider />
    <YoutubeSearch />
    <YoutubeTag />
    <YoutubeCont :youtubes="youtubes" />
  </div>
</template>
<script>
// @ is an alias to /src
import ContTitle from "@/components/layout/ContTitle.vue";
import YoutubeSlider from "@/components/youtube/YoutubeSlider.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import { ref } from "vue";

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

    const TopYoutubes = async () => {
      await fetch(
        "https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=30&q=%EC%BD%94%EB%94%A9%EC%95%A0%ED%94%8C&type=video&key=AIzaSyDu13VB1Y6cnu4y9DKqA3bLgAXuqaw4BFU"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result.items);
          youtubes.value = result.items;
        })
        .catch((error) => console.log("error", error));
    };
    TopYoutubes();
    return {
      youtubes,
      TopYoutubes,
    };
  },
};
</script>
