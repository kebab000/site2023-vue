<template>
  <header
    id="header"
    class="header__wrap nexon5 bg-vue"
    role="heading"
    aria-level="1"
  >
    <div class="header__inner container">
      <h1 class="header__logo">
        <router-link to="/"> VUE <em>SITE</em> </router-link>
      </h1>
      <nav class="header__nav" role="navigation">
        <ul>
          <li>
            <router-link to="intro">INTRO</router-link>
          </li>
          <li>
            <router-link to="port">PORTFOLIO</router-link>
          </li>
          <li>
            <router-link to="youtube">YOUTUBE</router-link>
          </li>
          <li>
            <router-link to="unsplash">UNSPLASH</router-link>
          </li>
          <li>
            <router-link to="movie">MOVIE</router-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
<style lang="scss">
// header__wrap
#header {
  background-color: #e9fef5a2;
}
.header__inner {
  text-align: center;

  .header__logo {
    width: 100%;

    a {
      font-size: 30px;
      display: inline-block;
      padding: 5px 5px 0 5px;
      margin: 5px 5px 0 5px;
      text-transform: uppercase;
      font-weight: 800;

      em {
        text-transform: uppercase;
        font-weight: 500;
      }
    }
  }
  .header__nav {
    width: 100%;

    ul {
      padding: 0 10%;
      display: flex;
      justify-content: space-between;

      li {
        a {
          display: inline-block;
          padding: 20px 10px;
          margin: 2px;
          position: relative;

          &::before {
            content: "";
            width: calc(100% - 20px);
            height: 2px;
            background-color: var(--color_body);
            position: absolute;
            left: 10px;
            bottom: 16px;
            transform: scaleX(0);
            transition: all 0.3s ease;
          }

          &:hover::before {
            transform: scaleX(1);
          }
        }
      }
    }
  }
}
</style>
