<template>
  <section id="portCont" class="ports__item section center bg-blue">
    <h3>포트폴리오 소개</h3>
    <p>웹쓰 30기 포트폴리오 모음집입니다.</p>
    <div class="port__inner container">
      <div class="port__btn"></div>
      <div class="port__cont">
        <div class="port" v-for="(port, index) in ports" :key="index">
          <figure class="port__header">
            <a :href="port.url" target="_blank" rel="noreferrer">
              <img
                :src="`./images/port/${port.portImg}`"
                :alt="`${port.name}포트폴리오`"
              />
            </a>
          </figure>
          <div class="port__body">
            <span>
              <img
                :src="`../images/member/${port.profileImg}`"
                :alt="port.name"
              />
            </span>
            <div>
              <h4>{{ port.name }}</h4>
              <p>{{ port.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      ports: [
        {
          name: "이요셉",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port00-min.png",
          url: "https://kebab-portfolio.web.app/",
          profileImg: "member106.svg",
        },
        {
          name: "진현미",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port01-min.png",
          url: "https://portfolio-hyunmi.netlify.app/",
          profileImg: "member80.svg",
        },
        {
          name: "천설희",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port05-min.png",
          url: "https://portfolio-313.web.app/",
          profileImg: "member05.svg",
        },
        {
          name: "장진용",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port02-min.png",
          url: "https://portfolio-cc509.web.app/",
          profileImg: "member02.svg",
        },
        {
          name: "김도현",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port03-min.png",
          url: "https://kdh-portfolio.netlify.app",
          profileImg: "member03.svg",
        },
        {
          name: "이양구",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port04-min.png",
          url: "https://leeyanggoo-portfolio.web.app/",
          profileImg: "member04.svg",
        },
        {
          name: "이승연",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port06-min.png",
          url: "https://dkdlelw-portfolio.web.app/",
          profileImg: "member06.svg",
        },
        {
          name: "김현빈",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port07-min.png",
          url: "https://portfolio-hyenobeen.netlify.app/",
          profileImg: "member07.svg",
        },
        {
          name: "정황우",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port08-min.png",
          url: "https://jhwportfolio.netlify.app/",
          profileImg: "member08.svg",
        },
        {
          name: "여다슬",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port09-min.png",
          url: "https://yds-portfo.web.app/",
          profileImg: "member09.svg",
        },
        {
          name: "이은지",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port10-min.png",
          url: "https://my-portfolio-vite.web.app/",
          profileImg: "member10.svg",
        },
        {
          name: "노지영",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port11-min.png",
          url: "https://noji-portfolio.netlify.app/",
          profileImg: "member11.svg",
        },
        {
          name: "이훈규",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port12-min.png",
          url: "https://hoongportfolio.netlify.app/",
          profileImg: "member107.svg",
        },
        {
          name: "신동진",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port13-min.png",
          url: "https://sdj-portfolio-5a461.web.app/",
          profileImg: "member13.svg",
        },
        {
          name: "김도현",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port15-min.png",
          url: "https://portfolio-45429.web.app/",
          profileImg: "member15.svg",
        },
        {
          name: "변우현",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port16-min.png",
          url: "https://fitalux-portfolio-vite-2023.netlify.app/",
          profileImg: "member16.svg",
        },
        {
          name: "안교남",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port17-min.png",
          url: "https://portfolio-18b72.web.app/",
          profileImg: "member17.svg",
        },
        {
          name: "전윤기",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port18-min.png",
          url: "https://myportpolio-e7f37.web.app",
          profileImg: "member18.svg",
        },
        {
          name: "권현정",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port19-min.png",
          url: "#",
          profileImg: "member19.svg",
        },
        {
          name: "정희석",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port20-min.png",
          url: "https://getgrovy-port.web.app/",
          profileImg: "member20.svg",
        },
        {
          name: "이유나",
          desc: "프론트앤드 개발자 포트폴리오",
          portImg: "port21-min.png",
          url: "https://yuna-portfolio.web.app/",
          profileImg: "member21.svg",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.ports__item {
  > p {
    margin-top: 10px;
  }
  .port__inner {
    .port__cont {
      @include flex-center;
      flex-wrap: wrap;
      .port {
        width: 32%;
        // overflow: hidden;
        .port__header {
          img {
            width: 98%;
            height: 200px;
            border-radius: 10px;
            object-fit: cover;
          }
        }
        .port__body {
          display: flex;
          margin-top: 15px;
          margin-bottom: 30px;
          position: relative;

          > span {
            img {
              border-radius: 50%;
              width: 50px;
              height: 50px;
            }
          }
          &::before {
            content: "";
            width: 50px;
            height: 50px;
            background-color: #0f035d;
            position: absolute;
            border-radius: 50%;
            top: 0;
            left: 0;
            z-index: -999;
          }
          > div {
            text-align: left;
            margin-left: 10px;
            h4 {
              font-size: 20px;
              font-weight: 400;
            }
            p {
              font-size: 16px;
              color: #2c3a4b;
            }
          }
        }
        &:nth-child(1) .port__body::before {
          background-color: #fa635c;
        }
        &:nth-child(2) .port__body::before {
          background-color: #fee580;
        }
        &:nth-child(3) .port__body::before {
          background-color: #d6d4ed;
        }
        &:nth-child(4) .port__body::before {
          background-color: #f4d6ba;
        }
        &:nth-child(5) .port__body::before {
          background-color: #b2b764;
        }
        &:nth-child(6) .port__body::before {
          background-color: #837673;
        }
        &:nth-child(7) .port__body::before {
          background-color: #c0a89d;
        }
        &:nth-child(8) .port__body::before {
          background-color: #f09f79;
        }
        &:nth-child(9) .port__body::before {
          background-color: #eee170;
        }
        &:nth-child(10) .port__body::before {
          background-color: #ed6e6e;
        }
        &:nth-child(11) .port__body::before {
          background-color: #fdd5c2;
        }
        &:nth-child(12) .port__body::before {
          background-color: #caf7bd;
        }
        &:nth-child(13) .port__body::before {
          background-color: #c8fbbd;
        }
        &:nth-child(14) .port__body::before {
          background-color: #b2d9f7;
        }
        &:nth-child(15) .port__body::before {
          background-color: #b3f8d2;
        }
        &:nth-child(16) .port__body::before {
          background-color: #def8e0;
        }
        &:nth-child(17) .port__body::before {
          background-color: #c1bbfa;
        }
        &:nth-child(18) .port__body::before {
          background-color: #dda5f5;
        }
        &:nth-child(19) .port__body::before {
          background-color: #71f791;
        }
        &:nth-child(20) .port__body::before {
          background-color: #f6cbd8;
        }
        &:nth-child(21) .port__body::before {
          background-color: #6ebcf1;
        }
      }
    }
  }
}
</style>
