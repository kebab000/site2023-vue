<template>
  <div className="youtube__cont">
    <ul>
      <li v-for="(youtube, index) in youtubes" :key="index">
        <a
          :href="`https://www.youtube.com/watch?v=${youtube.id.videoId}`"
          target="_blank"
        >
          <img
            :src="youtube.snippet.thumbnails.medium.url"
            :alt="youtube.snippet.title"
          />
          <span>{{ youtube.snippet.title }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang="scss" scoped>
.youtube__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 24%;
      margin-bottom: 4%;

      img {
        width: 100%;
        object-fit: cover;
      }
      span {
        display: block;
        margin: 4px 0;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        -webkit-line-clamp: 1; /* 라인수 */
      }
    }
  }
}
</style>
