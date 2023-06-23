<template>
  <div class="movie__tag">
    <ul>
      <li>
        <a @click="onClick('https://api.themoviedb.org/3/movie/popular')"
          >인기 영화</a
        >
      </li>
      <li>
        <a @click="onClick('https://api.themoviedb.org/3/movie/now_playing')"
          >현재 상영작</a
        >
      </li>
      <li>
        <a @click="onClick('https://api.themoviedb.org/3/tv/popular')"
          >인기 TV 쇼</a
        >
      </li>
      <li>
        <a @click="onClick('https://api.themoviedb.org/3/tv/top_rated')"
          >TV 쇼 순위</a
        >
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    onClick(value) {
      this.$emit("on-search", value);
    },
  },
};
</script>
<style lang="scss">
.movie__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;
    li {
      a {
        border: 1px solid #990df7;
        padding: 10px 20px;
        margin: 0 10px;
        color: #990df7;
        cursor: pointer;

        &:hover {
          color: #ffffff;
          background-color: #990df7;
        }
      }
    }
  }
}
</style>
