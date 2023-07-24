<template>
  <div className="intro__items bg-blue nexon5">
    <h2>내가 만든 사이트 모음</h2>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        <a :href="item.url" target="_blank" rel="noreferrer">
          <img :src="`./images/introPage/${item.src}`" :alt="item.title" />
          <span>{{ item.title }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      intros: [
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider00-min.jpeg",
          title: "프로필 사진",
        },
        {
          src: "introSlider01-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider02-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider03-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider04-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider05-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider06-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider07-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider08-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider09-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider10-min.jpg",
          title: "프로필 사진",
        },
        {
          src: "introSlider11-min.jpg",
          title: "프로필 사진",
        },
      ],
    };
  },
};
</script>
<styel lang="scss">
// intro item
.intro__items {
  padding: 30px;
  h2 {
    font-size: 50px;
    text-align: center;
    margin-bottom: 30px;
  }
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
        height: 200px;
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
</styel>
