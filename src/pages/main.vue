<template>
  <div class="view">
    <div class="header">
      <h3>年度账单</h3>
    </div>
    <div class="fixed-hint" v-if="showFixedHint">
      <i class="triangle-icon triangle-icon-small"></i>
      <i class="triangle-icon triangle-icon-big"></i>
      <span>向上滑，查看年账单</span>
    </div>
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide class="page01">
        <div class="detail-page">
          <div class="text-detail-box" :class="thisActiveIndex == 0 ? 'have-animation' : ''">
            <p class="font-title-color">时光总是偷偷流流逝</p>
            <p class="font-title-color">转眼间一年又过去了</p>
            <p class="font-title-color">打开支付宝账单</p>
            <p class="font-important-color font-bold margin-top-5px">这一年你又被坑了多少钱呢？</p>
          </div>
          <video
            id="video14"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/2-1.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
      <swiper-slide class="page02">
        <div class="detail-page">
          <div class="text-detail-box text-detail-box-01" :class="thisActiveIndex == 1 ? 'animated flipInX' : ''">
            <p class="font-important-color">2019年</p>
            <p class="font-title-color">你更爱买化妆品类</p>
            <p class="font-title-color">商品共花费100万元</p>
					  <p class="font-title-color">用剁手来表达爱</p>
          </div>
          <div class="text-detail-box text-detail-box-02" :class="thisActiveIndex == 1 ? 'animated flipInY' : ''">
            <p class="font-title-color">网购总支出1000万</p>
					  <p class="font-title-color">服饰类28%；旅游21%；通信1%；</p>
          </div>
          <video
            id="video1"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/1-2.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
          <video
            id="video13"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/3-2.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
      <swiper-slide class="page03">
        <div class="detail-page">
          <div class="text-detail-box text-detail-box-01" :class="thisActiveIndex == 2 ? 'animated bounceInLeft' : ''">
            <p class="font-important-color">2019年</p>
            <p class="font-title-color">你更爱买化妆品类</p>
            <p class="font-title-color">商品共花费100万元</p>
					  <p class="font-title-color">用剁手来表达爱</p>
          </div>
          <div class="text-detail-box text-detail-box-02" :class="thisActiveIndex == 2 ? 'animated bounceInUp' : ''">
            <p class="font-title-color">网购总支出1000万</p>
					  <p class="font-title-color">服饰类28%；旅游21%；通信1%；</p>
          </div>
          <video
            id="video2"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/2-3.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
          <video
            id="video12"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/4-3.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
      <swiper-slide class="page04">
        <div class="detail-page">
          <video
            id="video3"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/3-4.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
          <video
            id="video11"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/5-4.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
      <swiper-slide class="page05">
        <div class="detail-page">
          <video
            id="video4"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/4-5.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
          <video
            id="video10"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/6-5.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
      <swiper-slide class="page06">
        <div class="detail-page">
          <video
            id="video5"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/5-6.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
          <video
            id="video9"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/7-6.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
      <swiper-slide class="page07">
        <div class="detail-page">
          <video
            id="video6"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/6-7.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
          <video
            id="video8"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/8-7.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
      <swiper-slide class="page08">
        <div class="detail-page">
          <div class="text-detail-box text-detail-box-01" :class="thisActiveIndex == 7 ? 'animated bounce' : ''">
            <p class="font-important-color">2019年过去了</p>
            <p class="font-title-color">不知不觉，我和xxx一起走过了<span class="font-col-blue">9999天</span></p>
            <p class="font-title-color">在习以为常的生活里，总有些简单而美好的相遇</p>
          </div>
          <video
            id="video7"
            preload="auto"
            width="100%"
            height="100%"
            muted="muted"
            x-webkit-airplay="true"
            webkit-playsinline="true"
            playsinline
            style="display: none;"
          >
            <source src="../assets/7-8.mp4" type="video/mp4" />您的浏览器不支持 HTML5 video 标签。
          </video>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper"
export default {
  components: {
    swiper,
    swiperSlide
  },
  data() {
    return {
      // 是否展示提示滑动文本
      showFixedHint: true,
      // 记录滑动前的slideIndex
      beforeSlideIndex: 0,
      // 记录当前swiper的activeIndex
      thisActiveIndex: 0,
      // swiper配置项
      swiperOption: {
        effect: "fade", // 淡入
        direction: "vertical", // 垂直切换选项
        autoplay: false, // 是否自动播放
        height: window.innerHeight, // 高
        width: window.innerWidth, //宽
        speed: 0, // 切换速度
        on: {
          slideChange: () => {
            // debugger;
            let swiper = this.$refs.mySwiper.swiper;
            let slideIndex = swiper.activeIndex;
            this.thisActiveIndex = slideIndex;
            // console.log(slideIndex);
            if (slideIndex - this.beforeSlideIndex > 0) {
              // 向下滑动
              if (slideIndex == "1") {
                this.playVideo("video1");
              } else if (slideIndex == "2") {
                this.playVideo("video2");
              } else if (slideIndex == "3") {
                this.playVideo("video3");
              } else if (slideIndex == "4") {
                this.playVideo("video4");
              } else if (slideIndex == "5") {
                this.playVideo("video5");
              } else if (slideIndex == "6") {
                this.playVideo("video6");
              } else if (slideIndex == "7") {
                this.showFixedHint = false;
                this.playVideo("video7");
              }
            } else {
              // 向上回滑
              this.showFixedHint = true;
              if (slideIndex == "6") {
                this.playVideo("video8");
              } else if (slideIndex == "5") {
                this.playVideo("video9");
              } else if (slideIndex == "4") {
                this.playVideo("video10");
              } else if (slideIndex == "3") {
                this.playVideo("video11");
              } else if (slideIndex == "2") {
                this.playVideo("video12");
              } else if (slideIndex == "1") {
                this.playVideo("video13");
              } else if (slideIndex == "0") {
                this.playVideo("video14");
              }
            }
            this.beforeSlideIndex = slideIndex;
          }
        }
      }
    };
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper;
    }
  },
  methods: {
    // 视频播放
    playVideo(DOM) {
      let ele = document.getElementById(DOM);
      ele.style.display = "block";
      ele.play();
      // 监听视频播放是否结束，结束隐藏当前视频
      ele.addEventListener("ended", function() {
        ele.style.display = "none";
      });
    }
  }
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  color: #fff;
}

html,
body {
  margin: 0;
  padding: 0;
}

.font-bold {
  font-weight: 600;
}

.font-important-color {
  color: #212121 !important;
}

.font-title-color {
  color: #424242 !important;
}

.font-col-blue {
  color: #33a3ff;
}

.margin-top-5px {
  margin-top: 5px;
}
</style>

<style lang="scss" scoped>
.view {
  .header {
    position: fixed;
    z-index: 10;
    display: block;
    height: 46px;
    line-height: 46px;
    top: 0;
    left: 0;
    right: 0;
    h3 {
      font-size: 16px;
      text-align: center;
      color: #ffffff;
      font-weight: 600;
    }
  }
  .fixed-hint {
    position: fixed;
    z-index: 10;
    padding-top: 60px;
    bottom: 10%;
    left: 50%;
    transform: translateX(-50%);
    font-size: 14px;
    font-weight: 600;
    animation: fixedHintAnimation 1s linear infinite;
    .triangle-icon {
      position: absolute;
      display: block;
      left: 50%;
      transform: translateX(-50%);
      width: 0;
      height: 0;
      &.triangle-icon-small {
        top: 0;
        border-bottom: 12px solid #fff;
        border-right: 8px solid transparent;
        border-left: 8px solid transparent;
      }
      &.triangle-icon-big {
        top: 30px;
        border-bottom: 18px solid #fff;
        border-right: 12px solid transparent;
        border-left: 12px solid transparent;
      }
    }
  }
  @keyframes fixedHintAnimation {
    0% {
      bottom: 10%;
      opacity: 0.5;
    }
    100% {
      bottom: 14%;
      opacity: 1;
    }
  }
  .detail-page {
    position: relative;
    display: block;
    width: 100%;
    height: 100%;
    .text-detail-box {
      position: absolute;
      display: inline-block;
      background-color: rgba(255, 255, 255, 0.8);
      padding: 10px 14px;
      border-radius: 10px;
      p {
        font-size: 14px;
        line-height: 20px;
      }
    }
  }
  .page01 {
    background: url(../assets/1.png) no-repeat;
    background-size: 100% 100%;
    .detail-page {
      .text-detail-box {
        top: 20%;
        left: 10%;
        &.have-animation {
          animation: page01Animation 1s linear;
        }
      }
    }
  }
  @keyframes page01Animation {
    0% {
      left: 0%;
      opacity: 0.2;
    }
    50% {
      left: 25%;
      opacity: 0.7;
    }
    100% {
      left: 10%;
      opacity: 1;
    }
  }
  .page02 {
    background: url(../assets/2.png) no-repeat;
    background-size: 100% 100%;
    .detail-page {
      .text-detail-box-01 {
        top: 20%;
        left: 10%;
      }
      .text-detail-box-02 {
        top: 50%;
        right: 10%;
      }
    }
  }
  .page03 {
    background: url(../assets/3.png) no-repeat;
    background-size: 100% 100%;
    .detail-page {
      .text-detail-box-01 {
        top: 20%;
        left: 10%;
      }
      .text-detail-box-02 {
        top: 50%;
        right: 10%;
      }
    }
  }
  .page04 {
    background: url(../assets/4.png) no-repeat;
    background-size: 100% 100%;
  }
  .page05 {
    background: url(../assets/5.png) no-repeat;
    background-size: 100% 100%;
  }
  .page06 {
    background: url(../assets/6.png) no-repeat;
    background-size: 100% 100%;
  }
  .page07 {
    background: url(../assets/7.png) no-repeat;
    background-size: 100% 100%;
  }
  .page08 {
    background: url(../assets/8.png) no-repeat;
    background-size: 100% 100%;
    .text-detail-box-01 {
      top: 30%;
      right: 10%;
    }
  }
}
</style>
