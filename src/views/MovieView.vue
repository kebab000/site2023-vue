<template>
  <div class="movie">
    <ContTitle title="movies" />
    <MovieSlider />
    <MovieSearch />
    <MovieTag />
    <MovieCont :movies="movies" />
  </div>
</template>
<script>
// @ is an alias to /src
import ContTitle from "@/components/layout/ContTitle.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    MovieSlider,
    MovieSearch,
    MovieTag,
    MovieCont,
  },

  setup() {
    const movies = ref([]);
    const searchs = ref([]);
    const search = ref(["marvel"]);

    const TopMovies = async () => {
      await fetch(
        `https://api.themoviedb.org/3/movie/popular?api_key=697729d3f274ce88cf5729d38280fd33&query=${search.value}`
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result.results);
          movies.value = result.results;
          searchs.value = result.results;
          console.log(searchs);
        })
        .catch((error) => console.log("error", error));
    };
    TopMovies();
    return {
      movies,
      searchs,
      TopMovies,
    };
  },
};
</script>
