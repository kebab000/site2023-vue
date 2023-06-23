<template>
  <div class="unsplash__tag">
    <ul>
      <li><a @click="onClick('nature')">자연 사진</a></li>
      <li><a @click="onClick('city')">도시 사진</a></li>
      <li><a @click="onClick('food')">음식 사진</a></li>
      <li><a @click="onClick('sky')">하늘 사진</a></li>
      <li><a @click="onClick('daily')">일상 사진</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    onClick(value) {
      this.$emit("onSearch", value);
    },
  },
};
</script>
<style lang="scss">
.unsplash__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;
    li {
      a {
        border: 1px solid #4857ec;
        padding: 10px 20px;
        margin: 0 10px;
        color: #4857ec;
        cursor: pointer;

        &:hover {
          color: #fff;
          background-color: #4857ec;
        }
      }
    }
  }
}
</style>
