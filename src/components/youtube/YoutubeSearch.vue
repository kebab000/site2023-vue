<template>
  <div class="youtube__search">
    <h2 class="blind">검색하기</h2>
    <input
      ref="inputRef"
      type="search"
      @keypress="onKeyPress"
      placeholder="동영상을 검색하세요!"
    />
    <button type="submit" @click="onClick">검색하기</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "YoutubeSearch",
  setup(props, { emit }) {
    const inputRef = ref(null);

    const handleSearch = () => {
      const value = inputRef.value.value;
      emit("onSearch", value);
    };

    const onKeyPress = (event) => {
      if (event.key === "Enter") {
        handleSearch();
      }
    };

    const onClick = () => {
      handleSearch();
    };

    return {
      inputRef,
      onKeyPress,
      onClick,
    };
  },
};
</script>
