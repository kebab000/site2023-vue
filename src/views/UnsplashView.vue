<template>
  <div class="unsplash">
    <ContTitle title="unsplash" />
    <UnsplashSlider />
    <UnsplashSearch />
    <UnsplashTag />
    <UnsplashCont :unsplashs="unsplashs" />
  </div>
</template>
<script>
// @ is an alias to /src
import ContTitle from "@/components/layout/ContTitle.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    UnsplashSlider,
    UnsplashSearch,
    UnsplashTag,
    UnsplashCont,
  },

  setup() {
    const unsplashs = ref([]);

    const Topunsplashs = async () => {
      await fetch(
        "https://api.unsplash.com/photos?client_id=Wy3aU02kZCmqZYm8bpmsgKBccb06xdDXsWYBEjOGnPE&"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          unsplashs.value = result;
        })
        .catch((error) => console.log("error", error));
    };
    Topunsplashs();
    return {
      unsplashs,
      Topunsplashs,
    };
  },
};
</script>
