<template>
  <section id="introSection" class="intro__wrap section bg-blue nexon5">
    <h3 class="blind">프론트앤드 커리큘럼 과정 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>Portfolio</span>
        <figure class="myCharacter">
          <img src="../../assets/images/member/member106.svg" alt="나" />
        </figure>
        <h3>이요셉</h3>
        <p>
          프론트앤드 개발자가 되기 위해 <br />
          준비중입니다!<br />
          Javascript, React, Next.js, <br />PHP, MYSQL등을 배웠습니다.
        </p>
      </div>
      <div class="intro__desc">
        <div>
          <router-link to="https://kebab00.tistory.com/"
            ><h4 class="icon-bg1">Tistory</h4></router-link
          >
          <p>
            수업을 시작하면서 개설한 Tistory 블로그 입니다. 그동안 배운 것들을
            모두 정리하고 복습한 사이트이며 HTML, CSS, PHP, JavaScript,
            Programmers등이 정리되어 있습니다.
          </p>
        </div>
        <div>
          <router-link to="https://github.com/kebab000/"
            ><h4 class="icon-bg2">Github</h4></router-link
          >
          <p>
            GitHub은 분산 버전 관리 시스템인 Git을 기반으로 하는 웹 기반 호스팅
            서비스입니다. 개발자들은 Git을 사용하여 소스 코드를 추적하고
            변경사항을 관리할 수 있으며, GitHub을 통해 이러한 코드를 온라인으로
            저장, 공유 및 협업할 수 있습니다. 수업시간에 했던 모든 것이 저장되어
            있습니다.
          </p>
        </div>
        <div>
          <router-link to="https://kebab000.github.io/web2023/"
            ><h4 class="icon-bg3">JavaScript</h4></router-link
          >
          <p>
            수업의 기초가 되었던 JavaScript사이트 입니다. 가장 기초부터 시작해서
            다양한 메서드까지 수업시간에 했던 모든 예제들이 올라가 있습니다.
          </p>
        </div>
        <div>
          <router-link to="http://kebab00.dothome.co.kr/php2/index.html"
            ><h4 class="icon-bg4">PHP</h4></router-link
          >
          <p>
            조별과제로 만든 php사이트입니다. Planty라는 사이트로 식물관리에 대한
            정보를 제공하며 자기의 식물을 저장하고 커뮤니티를 통해 공유할 수
            있습니다.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
// intro__wrap
.intro__inner {
  display: flex;
  justify-content: space-between;
}
.intro__title {
  width: 33%;
  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }
  .myCharacter {
    position: relative;
    width: 230px;
    height: 290px;
    border: 1px solid #000;
    img {
      position: absolute;
      left: 0px;
      top: 5px;
    }
  }
  h3 {
    font-size: 50px;
    font-weight: 700;
    line-height: 1.2;
    margin-top: 10px;
    margin-bottom: 20px;
  }
  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}
.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  font-size: 18px;

  justify-content: space-between;

  > div {
    width: 48%;
    margin-bottom: 40px;

    h4 {
      font-size: 24px;
      margin-bottom: 15px;
    }
    &:nth-child(3) {
      margin-bottom: 0;
    }
    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
