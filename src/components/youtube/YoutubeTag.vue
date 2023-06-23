<template>
  <div class="youtube__tag">
    <ul>
      <li><a @click="onClick('코딩 애플')">코딩 애플</a></li>
      <li><a @click="onClick('react.js')">react.js</a></li>
      <li><a @click="onClick('Next.js')">Next.js</a></li>
      <li><a @click="onClick('JavaScript')">JavaScript</a></li>
      <li><a @click="onClick('프론트앤드')">프론트앤드</a></li>
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
.youtube__tag {
  // display: none

  ul {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;
    li {
      a {
        border: 1px solid #f7100d;
        padding: 10px 20px;
        margin: 0 10px;
        color: #f7100d;
        &:hover {
          color: #fff;
          background-color: #f7100d;
        }
      }
    }
  }
}
</style>
