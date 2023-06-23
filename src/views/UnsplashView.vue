<template>
  <div>
    <ContTitle title="Unsplash" />
    <UnsplashSlider :images="images" />
    <UnsplashSearch @onSearch="search" />
    <UnsplashTag @onSearch="search" />
    <UnsplashCont :images="images" />
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import { ref, onMounted } from "vue";

export default {
  name: "UnsplashPage",
  components: {
    ContTitle,
    UnsplashSlider,
    UnsplashSearch,
    UnsplashTag,
    UnsplashCont,
  },
  setup() {
    const images = ref([]);

    const search = async (query) => {
      try {
        const response = await fetch(
          `https://api.unsplash.com/search/photos?client_id=Wy3aU02kZCmqZYm8bpmsgKBccb06xdDXsWYBEjOGnPE&per_page=30&query=${query}`
        );
        const result = await response.json();
        images.value = result.results;
      } catch (error) {
        console.log("error", error);
      }
    };

    onMounted(async () => {
      try {
        const response = await fetch(
          "https://api.unsplash.com/photos?client_id=Wy3aU02kZCmqZYm8bpmsgKBccb06xdDXsWYBEjOGnPE&"
        );
        const result = await response.json();
        images.value = result;
      } catch (error) {
        console.log("error", error);
      }
    });

    return {
      images,
      search,
    };
  },
};
</script>
