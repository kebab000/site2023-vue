<template>
  <section id="memberSection" class="members__wrap section center nexon5">
    <h3>멤버소개</h3>
    <p>함께 공부한 웹쓰 30기 멤버들 입니다.</p>
    <div class="member__inner container">
      <div class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/member80.svg" alt="땡땡님" />
        </figure>
        <div class="member__body">
          <h4 class="title">웹쓰30기</h4>
          <p class="desc">진현미</p>
          <router-link to="/" class="btn"></router-link>
        </div>
      </div>
      <div class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/member02.svg" alt="땡땡님" />
        </figure>
        <div class="member__body">
          <h4 class="title">웹쓰30기</h4>
          <p class="desc">김도현</p>
          <router-link to="/" class="btn"></router-link>
        </div>
      </div>
      <div class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/member03.svg" alt="땡땡님" />
        </figure>
        <div class="member__body">
          <h4 class="title">웹쓰30기</h4>
          <p class="desc">이양구</p>
          <router-link to="/" class="btn"></router-link>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
// members__wrap

.member__inner {
  @include flex-between;

  .member {
    width: 32%;
    border: 2px solid var(--color_body);

    .member__header {
      margin-top: -20px;
      padding: 20px;
      img {
        width: 100%;
      }
    }
    .member__body {
      margin-top: -90px;
      padding: 15px 10px;
      background: #000;
      color: #fff;
      z-index: 100;
      position: relative;

      h4 {
        font-size: 22px;
      }
      a {
        color: #fff;
        text-decoration: underline;
        text-underline-position: under;
      }
    }
  }
}
</style>
