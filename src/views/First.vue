<template>
  <div class="container">
    <ul ref="containerRef" class="container-ul">
      <!-- 第一个页面 -->
      <li class="first">
        <img src="./img/cover.325af244.jpg" alt="" />
        <div class="btn" @click="firstTo">
          <img src="./img/start1.5e2a29d0.png" alt="" />
        </div>
        <div class="btn" @click="twoTo">
          <img src="./img/start2.5091ff99.png" alt="" />
        </div>
      </li>
      <li
        class="two"
        v-if="controlPage1"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <img src="./img/p21.dfe5cfde.png" alt="" />
        <div class="btn-group">
          <button @click="firstTo">控制饮食</button>
          <button @click="firstTo">运动健身</button>
          <button @click="firstTo">民间偏方</button>
          <button @click="firstTo">改善两性关系，稳固感情</button>
        </div>
      </li>
      <!-- 被我漏掉的第二页 -->
      <li
        class="threePro"
        v-if="controlPage2"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <img src="./img/n3ndfn.png" alt="" />
        <div class="btn-group">
          <button @click="firstTo">毫无效果</button>
          <button @click="firstTo">有一点用，达不到理想</button>
          <button @click="firstTo">有一点用，坚持不下来</button>
          <!-- <button @click="firstTo">改善两性关系，稳固感情</button> -->
        </div>
      </li>
      <li
        class="three"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <img src="./img/p3.6bf15125.png" alt="" />
        <div class="btn-group">
          <button @click="firstTo">18-25岁</button>
          <button @click="firstTo">26-35岁</button>
          <button @click="firstTo">36-45岁</button>
          <button @click="firstTo">45岁以上</button>
        </div>
      </li>
      <li
        class="four"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <img src="./img/p41.d160e94f.png" alt="" />
        <div class="btn-group">
          <div class="answer" @click="firstTo('img/A1.174b0489.jpeg')">
            <img src="./img/A1.jpeg" alt="" />
          </div>
          <div class="answer" @click="firstTo('img/A2.71132a08.jpg')">
            <img src="./img/A2.jpg" alt="" />
          </div>
          <div class="answer" @click="firstTo('img/A3.ffb77aff.jpeg')">
            <img src="./img/A3.jpeg" alt="" />
          </div>
          <div class="answer" @click="firstTo('img/A4.06c3576b.jpg')">
            <img src="./img/A4.jpg" alt="" />
          </div>
        </div>
      </li>
      <li
        class="five"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <img src="./img/p5.bd0fc7f2.png" alt="" />
        <div class="btn-group">
          <button @click="firstTo">1年以内</button>
          <button @click="firstTo">1-3年</button>
          <button @click="firstTo">3-5年</button>
          <button @click="firstTo">5年以上</button>
        </div>
      </li>
      <li
        class="six"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <img src="./img/p61.7d3744fa.png" alt="" />
        <div class="btn-group">
          <div class="answer" @click="firstTo('img/B1.f59f3863.png')">
            <img src="./img/B1.png" alt="" />
          </div>
          <div class="answer" @click="firstTo('img/B2.ca7dbed9.png')">
            <img src="./img/B2.png" alt="" />
          </div>
          <div class="answer" @click="firstTo('img/B3.2d9747e0.png')">
            <img src="./img/B3.png" alt="" />
          </div>
          <div class="answer" @click="firstTo('img/B4.b13fedc6.png')">
            <img src="./img/B4.png" alt="" />
          </div>
        </div>
      </li>
      <li
        class="seven"
        ref="sevenRef"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <img src="./img/p11.3b9bd7dc.png" alt="" />
        <div class="btn-group">
          <button @click="firstTo">每天夜宵</button>
          <button @click="firstTo">暴饮暴食</button>
          <button @click="firstTo">爱吃甜品，油炸食品</button>
          <button @click="firstTo">以上都没有</button>
        </div>
      </li>
      <li
        class="eight"
        @touchstart="touchStar2"
        @touchmove="touchMove2"
        @touchend="touchEnd2"
        ref="Eight"
      >
        <img src="./img/info.76387460.png" alt="" />
        <div class="info-container">
          <p class="info-title">
            身高
            <small>cm</small>
          </p>
          <div class="info-content-outside">
            <span class="info-content-line"></span>
            <div class="tizhong" ref="wrapper2">
              <div
                class="info-content-side"
                ref="weightRef2"
                @touchstart="c"
                @touchend="d"
              >
                <div
                  class="info-content-item"
                  v-for="(item, index) in num1"
                  v-bind:key="index"
                >
                  {{ item }}
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="info-container">
          <p class="info-title">
            体重
            <small>kg</small>
          </p>
          <!-- 
            @touchstart="weightScollStar"
              @touchmove="weightScrolling"
              @touchend="weightScrollEnd"
           -->
          <div class="info-content-outside">
            <span class="info-content-line"></span>
            <div class="tizhong" ref="wrapper">
              <div
                class="info-content-side"
                ref="weightRef"
                @touchstart="a"
                @touchend="b"
              >
                <div
                  class="info-content-item"
                  v-for="(item, index) in num2"
                  v-bind:key="index"
                >
                  {{ item }}
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="info-container">
          <p class="info-title">
            腰围
            <small>cm</small>
          </p>
          <div class="info-content-outside ">
            <span class="info-content-line"></span>
            <div class="tizhong" ref="wrapper3">
              <div
                class="info-content-side aaaa"
                ref="weightRef3"
                @touchstart="e"
                @touchend="f"
              >
                <div
                  class="info-content-item"
                  v-for="(item, index) in num3"
                  v-bind:key="index"
                >
                  {{ item }}
                </div>
              </div>
            </div>
          </div>
        </div>
        <button class="btn-submit" @click="firstTo">提交</button>
      </li>
      <li
        class="night"
        @touchstart="touchStar"
        @touchmove="touchMove"
        @touchend="touchEnd"
      >
        <div class="result-bg">
          <span>
            已为你生成最终专属方案
          </span>
          <img :src="lastImg[1]" alt="" />
          <img :src="lastImg[3]" alt="" class="img2" />
          <!-- <img :src="lastImg[1]" alt="" />
          <img :src="lastImg[3]" alt="" class="img2" /> -->
          <p>调理前</p>
          <p>调理后</p>
        </div>
        <div class="result-text">
          <p>点击添加老师Line: <strong name="notweixin">sdfsdd</strong></p>
          <p>领取方案,老师将为你进行一对一指导</p>
        </div>
        <div class="contact-btn">
          <button class="selector" id="submit">
            点击添加老师Line
          </button>
        </div>
        <div class="result carousel-info">
          <div class="swiper-warpper">
            <div class="swiper-slide">
              <span>西西</span>
              <span>刚刚领取专属护理方案</span>
            </div>
            <div class="swiper-slide">
              <span>Alina</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>雨萱</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>kiko</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>倩怡</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>雅雯</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>Anni</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>Jolin</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>秀婉</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>欣欣</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>熙慧</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>敏瑶</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
            <div class="swiper-slide">
              <span>心倩</span>
              <span>刚刚领取专属丰胸方案</span>
            </div>
          </div>
        </div>
      </li>
    </ul>
    <div></div>
  </div>
</template>

<script>
// 这里出现一个问题，就是在vue文件中如何向不使用框架时的那种引法，还是这里要使用别的方式

//

let arr1 = []
let arr2 = []
let arr3 = []
for (let i = 140; i < 201; i++) {
  arr1.push(i)
}
for (let i = 35; i < 96; i++) {
  arr2.push(i)
}
for (let i = 50; i < 121; i++) {
  arr3.push(i)
}
let width3 = 77 * 56 + 180
let width1 = 64 * 56 + 110
let width2 = 74 * 56 + 110
import BScroll from 'better-scroll'
export default {
  created() {
    this.$nextTick(() => {
      this.personScroll()
      this.personScroll2()
      this.personScroll3()
    })
  },
  mounted() {
    const that = this
    window.onresize = () => {
      return (() => {
        window.screeWidth = document.body.clientWidth
        that.screeWidth = window.screeWidth
      })()
    }
  },

  data() {
    return {
      num1: arr1,
      num2: arr2,
      num3: arr3,
      controlNum: 1,
      controlPage1: true,
      controlPage2: true,
      starX: 0,
      endX: 0,
      // 控制往回退时的controlNum
      controlNum3: 2,
      // 表示全部的轮播图的页面距离
      allContainer: 0,
      // 这里设置一个判断是否是进入第二分支的判断两
      isTwo: false,
      // 表示身高的滑动时点击的那个位置的点
      heightStarX: 0,
      // 表示身高的滑动时结束的那个位置的点
      heightEndX: 0,
      //身高的滑动总
      heightSum: 0,
      // 使得高度的开始时的获取位置只计算一次的
      heigthNum: 1,
      // 体重的开始的点击的位置的点
      weightStarX: 0,
      // 体重的总
      weightSum: 1,
      // 体重的滑动结束时的那个位置的点
      weightEndX: 0,
      // 胸围的开始的点击的位置的点
      bustStarX: 0,
      // 胸围的结束的点击的位置的点
      bustEndX: 0,
      // 胸围的总
      bustNum: 0,
      // 方法A=>体重
      A: true,
      // 方法B=>身高
      B: true,
      // 方法C=>胸围
      C: true,
      // 最终显示的那两张图片的数组
      lastImg: [],

      numImg: 2,
    }
  },
  methods: {
    // 最终加载滑动的方法
    a(e) {
      this.A = false
    },
    // 停止滑动时的回复
    b() {
      this.A = true
    },
    c() {
      this.B = false
    },
    d() {
      this.B = true
    },
    e() {
      this.C = false
    },
    f() {
      this.C = true
    },
    // 一个横向滚动的方法

    //那个横向滚动的
    personScroll() {
      // 默认有六个li子元素，每个子元素的宽度为120px

      this.$refs.weightRef.style.width = width1 + 'px'
      // this.$nextTick 是一个异步函数，为了确保 DOM 已经渲染
      this.$nextTick(() => {
        if (!this.scroll) {
          this.scroll = new BScroll(this.$refs.wrapper, {
            startX: 0,
            click: true,
            scrollX: true,
            // 忽略竖直方向的滚动
            scrollY: false,
            eventPassthrough: 'vertical',
          })
        } else {
          this.scroll.refresh()
        }
      })
    },
    personScroll2() {
      // 默认有六个li子元素，每个子元素的宽度为120px

      this.$refs.weightRef2.style.width = width2 + 'px'
      // this.$nextTick 是一个异步函数，为了确保 DOM 已经渲染
      this.$nextTick(() => {
        if (!this.scroll2) {
          this.scroll2 = new BScroll(this.$refs.wrapper2, {
            startX: 0,
            click: true,
            scrollX: true,
            // 忽略竖直方向的滚动
            scrollY: false,
            eventPassthrough: 'vertical',
            probeType: 3,
          })
        } else {
          this.scroll2.refresh()
        }
      })
    },
    personScroll3() {
      // 默认有六个li子元素，每个子元素的宽度为120px

      this.$refs.weightRef3.style.width = width3 + 'px'
      // this.$nextTick 是一个异步函数，为了确保 DOM 已经渲染
      this.$nextTick(() => {
        if (!this.scroll3) {
          this.scroll3 = new BScroll(this.$refs.wrapper3, {
            startX: 0,
            click: true,
            scrollX: true,
            // 忽略竖直方向的滚动
            scrollY: false,
            eventPassthrough: 'vertical',
          })
        } else {
          this.scroll3.refresh()
        }
      })
    },
    // 有减肥经验的
    firstTo(img) {
      if (img && img !== null) {
        this.lastImg.push(arguments[0])
      }
      if (this.controlNum <= 9) {
        // this.isTwo = false

        this.allContainer = this.allContainer + 100

        this.$refs.containerRef.style.left = `-${this.allContainer}%`
      }
    },
    twoTo() {
      this.controlPage1 = false
      this.controlPage2 = false
      this.allContainer = this.allContainer + 100
      if (this.isTwo && this.allContainer > 700) {
        this.allContainer = 700
      }
      this.$refs.containerRef.style.left = `-${this.allContainer}%`
      this.isTwo = true
    },
    // 第八页的特殊令起一个方法
    touchStar2(e) {
      if (this.A && this.B && this.C) {
        this.starX = e.touches[0].clientX
        // console.log(this.starX)
      }
    },
    // 移动时记录手指的位置
    touchMove2(e) {
      if (this.A && this.B && this.C) {
        this.endX = this.starX - e.touches[0].clientX

        if (this.endX < 0) {
          this.controlNum3--
          if (this.controlNum3 == 1) {
            this.controlNum3--

            this.allContainer = this.allContainer - 100
            this.$refs.containerRef.style.left = `-${this.allContainer}%`
          }
        }
      }
    },
    touchEnd2(e) {
      if (this.A && this.B && this.C) {
        this.controlNum3 = 2

        let instance = this.$refs.containerRef.style.left

        if (this.isTwo && instance == '0%') {
          this.$refs.containerRef.style.left = '0px'
          setTimeout(() => {
            this.controlPage1 = true
            this.controlPage2 = true
          }, 300)

          this.allContainer = 0
        }
      }
    },
    // -end
    // 刚开始滑动时记录一开始的手指的位置
    touchStar(e) {
      this.starX = e.touches[0].clientX
      // console.log(this.starX)
    },
    // 移动时记录手指的位置
    touchMove(e) {
      this.endX = this.starX - e.touches[0].clientX

      if (this.endX < 0) {
        this.controlNum3--
        if (this.controlNum3 == 1) {
          this.controlNum3--

          this.allContainer = this.allContainer - 100
          this.$refs.containerRef.style.left = `-${this.allContainer}%`
        }
      }
    },
    touchEnd(e) {
      this.controlNum3 = 2

      let instance = this.$refs.containerRef.style.left

      if (this.isTwo && instance == '0%') {
        this.$refs.containerRef.style.left = '0px'
        setTimeout(() => {
          this.controlPage1 = true
          this.controlPage2 = true
        }, 300)

        this.allContainer = 0
      }
    },

    // 开始
    bustScollStar(e) {
      if (this.bustNum == 1) {
        e.stopPropagation()
        this.bustStarX = this.bustStarX - e.touches[0].clientX
        this.bustNum--
      }
    },
    // 过程
    bustScolling(e) {
      e.stopPropagation()
      this.bustEndX = this.bustStarX - e.touches[0].clientX
      if (this.bustEndX < 0) {
        if (this.bustEndX < -2800) {
          this.bustEndX = 1
        }
        this.$refs.bustRef.style.left = `${this.bustEndX}px`
      } else {
        if (this.bustEndX > 404) {
          this.bustEndX = 404
        }
        this.$refs.bustRef.style.left = `${this.bustEndX + 100}px`
        // console.log(this.bustEndX)
      }
    },
    // 结束
    bustScrollEnd() {
      this.bustStarX = this.bustEndX + 100
      // console.log(this.bustEndX)
    },
  },
  // 身高的滑动开始时的触摸
}
</script>

<style lang="less" scoped>
.tizhong {
  // height: 100%;
  padding: 17px 0;
}
// 到数第二页的文字的滚动
.swiper-warpper {
  animation: myMove 18s linear infinite;
  animation-fill-mode: forwards;
}
// 文字动画效果的效果
@keyframes myMove {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-520px);
  }
}

// 媒体查询
// 共有的button点击样式
button:active {
  background-color: #ee4f67 !important;
  color: #ffffff !important;
}
.answer:active {
  border: 4px solid #ee4f67 !important;
}
// 整个容器的样式

* {
  box-sizing: border-box;
}
.container {
  // width: 100vw;
  // height: 100vh;
  // overflow: hidden;
  position: relative;
  width: 100%;
  max-width: 750px;
  height: 100vh;
  margin: 0 auto;
  // transition: left 3s ease-out;
  overflow: hidden;

  ul {
    width: 1000%;
    height: 100vh;

    li {
      float: left;
      min-height: 100vh;
      max-height: 100vh;
    }
  }
}
// 整个轮播图ul
.container-ul {
  transition: left 0.6s ease-out;
  position: relative;
  left: 0;
}
// 第二个页面的样式
.two,
.three,
.threePro,
.five,
.seven {
  background: url('./img/bg.c8f22030.png') no-repeat;
  background-size: 100% 100%;
  width: 100vw;
  height: 100vh;
  img {
    width: 100%;
    margin-top: 32px;
  }
  .btn-group {
    margin-top: 16px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    button + button {
      margin-top: 16px;
    }
    button {
      display: inline-flex;
      width: 82%;
      height: 55px;
      align-items: center;
      justify-content: center;
      outline: none;
      border: 3px solid #ffa8b5;
      border-radius: 6px;
      background-color: #fff;
      color: #ee4f67;
      font-size: 17px;
      font-weight: 700;
      box-shadow: 2px 4px 3px rgba(0, 0, 0, 0.2);
    }
  }
}
// 第四个页面
.four,
.six {
  background: url('./img/bg.c8f22030.png') no-repeat;
  background-size: 100% 100%;
  width: 100vw;
  height: 100vh;
  > img {
    width: 100%;
    margin-top: 32px;
  }
  .btn-group {
    // margin-top: -16px;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    .answer {
      border: 3px solid #ffa8b5;
      border-radius: 6px;
      background-color: #fff;
      box-shadow: 2px 4px 3px rgba(0, 0, 0, 0.2);
      width: 38vw;
      height: 38vw;
      margin: 4px;
      img {
        width: 100%;
        height: 100%;
        object-fit: contain;
        object-position: center;
      }
    }
  }
}
// 第八个页面（到数第二个页面）
.info-container {
  margin: 0 auto;
  width: 85%;
  height: 50px;
  display: flex;
  .info-title {
    flex-grow: 1;
    // line-height: 50px;
    font-size: 20px;
    font-weight: 700;
    color: #fff;
    -webkit-text-stroke: 0.6px #000;
    small {
      font-size: 12px;
    }
  }

  .info-content-outside {
    position: relative;
    border-radius: 6px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.2);
    box-shadow: 1px 1px 6px rgba(0, 0, 0, 0.3);
    background-color: #faa8b6;
    width: 80%;
    overflow: hidden;
    .info-content-line {
      display: block;
      position: absolute;
      width: 0.5px;
      height: 100%;
      left: 55%;
      top: 0;
      transform: translate(-50%);
      background-color: #a2eb10;
    }

    .info-content-side {
      padding: 0 10px 0 110px;

      transform: translate3d(-394.8px, 0px, 0px);

      margin: 0 auto;
      // position: relative;
      // width: 100%;
      // height: 100%;
      z-index: 1;
      display: flex;
      transition-property: transform;
      box-sizing: content-box;

      .info-content-item {
        padding: 0 20px;
        // display: inline-flex;
        align-items: center;
        justify-content: center;
        color: #fff;
        font-weight: 500;
        height: 100%;
        flex-shrink: 0;
        position: relative;
        transition-property: transform;
      }
    }
    .aaaa {
      // padding: 0 10px 0 170px;
      transform: translate3d(-904.8px, 0px, 0px);
    }
  }
}
.btn-submit {
  margin-top: 48px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  outline: none;
  border: 2px solid #ffa8b5;
  border-radius: 6px;
  width: 70%;
  height: 50px;
  background-color: #fff;
  color: #ee4f67;
  font-size: 16px;
  position: relative;
  left: 50%;
  transform: translateX(-50%);
}
.info-container + .info-container {
  margin-top: 32px;
}
.eight {
  background: url('./img/bg.c8f22030.png') no-repeat;
  background-size: 100% 100%;
  width: 100vw;
  height: 100vh;
  img {
    width: 100%;
    margin-top: 32px;
  }
}
// 第九个页面
.night {
  background: url('./img/bg.c8f22030.png') no-repeat;
  background-size: 100% 100%;
  width: 100vw;
  height: 100vh;
  img {
    width: 100%;
    margin-top: 32px;
  }
  .result-bg {
    width: 100%;
    height: 60%;
    max-height: 400px;
    background-image: url('./img/result-bg.b51c38f9.png');
    background-size: contain;
    background-repeat: no-repeat;
    background-position: top;
    position: relative;
    span {
      font-size: 22px;
      font-weight: 700;
      position: absolute;
      top: 45%;
      left: 50%;
      transform: translateX(-50%);
      right: 0;
      width: 250px;
    }
    img {
      width: 30%;
      padding: 0 4px;
      border: 2px solid #ffa8b5;
      border-radius: 6px;
      box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
      background-color: #fff;
      position: absolute;
      top: 48%;
      left: 14vw;
    }
    .img2 {
      left: 51vw;
      height: 116px;
    }
    p {
      font-size: 16px;
      position: absolute;
      bottom: 3%;
    }
    p:first-of-type {
      left: 23.5%;
    }
    p:last-of-type {
      right: 23.5%;
    }
  }
  .result-text {
    margin-top: 24px;
    font-size: 16px;
    font-weight: 700;
    p {
      margin: 0 auto;
      text-align: center;
    }
    p + p {
      margin-top: 5px;
    }
  }
  .contact-btn {
    width: 85%;
    margin: 24px auto 0;
    display: flex;
    justify-content: center;
    align-items: center;
    ::before {
      content: '';
      display: inline-block;
      width: 40px;
      height: 40px;
      background-image: url('./img/line.png');
      background-size: contain;
      background-repeat: no-repeat;
      background-position: 50%;
      margin: 0 4px 0 -12px;
    }
    button {
      margin-left: 0px !important;
      width: 240px !important;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 140px;
      height: 45px;
      outline: none;
      border: none;
      border-radius: 4px;
      color: #fff;
      font-size: 14px;
      font-weight: 700;
      background-image: linear-gradient(
        180deg,
        #e24c63,
        #f75b72,
        #ee4f67 98%,
        hsla(0, 0%, 100%, 0.3)
      );
    }
    .selector {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 140px;
      height: 45px;
      outline: none;
      border: none;
      border-radius: 4px;
      color: #fff;
      font-size: 14px;
      font-weight: 700;
      background-image: linear-gradient(
        180deg,
        #e24c63,
        #f75b72,
        #ee4f67 98%,
        hsla(0, 0%, 100%, 0.3)
      );
    }
  }
  .result {
    border-bottom: 1px solid #f7536b;
    border-radius: 4px;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2);
    background-color: #fff;
    margin: 24px auto 0;
    width: 70%;
    height: 40px;
    overflow: hidden;
    .swiper-warpper {
      position: relative;
      width: 100%;
      height: 100%;
      z-index: 1;
      display: flex;
      flex-wrap: wrap;
      transition-property: transform;
      box-sizing: content-box;
      .swiper-slide {
        margin: 2px 0;
        padding: 0 16px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 100%;
        flex-shrink: 0;
        position: relative;
        transition-property: transform;
      }
    }
  }
}

/* 样式初始化 */
body {
  height: 100%;
}
li {
  list-style: none;
}
ul,
li {
  padding: 0;
  margin: 0;
}
.first {
  width: 100vw;
  height: 100vh;
  max-width: 750px;
  position: relative;
  // max-height: 100vh;
  // background: url('./img/cover.325af244.jpg') no-repeat;
  // background-size: 100% 100%;
  > img {
    width: 100%;
    height: 100%;
  }

  // margin: 0 auto;
}
/* 动画按钮 */
.btn {
  position: absolute;
  z-index: 100;
  bottom: 2vh;
  width: 40%;
}

.btn img {
  width: 100%;
}

.btn:first-of-type {
  left: 6%;
  -webkit-animation: init1 2s 0s infinite;
  animation: init1 2s 0s infinite;
}

.btn:first-of-type:before {
  content: '';
  position: absolute;
  z-index: -1;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border: 10px solid hsla(0, 0%, 100%, 0.4);
  border-radius: 50%;
  width: 80%;
  height: 80%;
  opacity: 0;
  -webkit-animation: ripple 2s 0.1s infinite;
  animation: ripple 2s 0.1s infinite;
}

.btn:last-of-type {
  right: 6%;
  -webkit-animation: init1 2s 0.3s infinite;
  animation: init1 2s 0.3s infinite;
}

.btn:last-of-type:before {
  content: '';
  position: absolute;
  z-index: -2;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border: 10px solid hsla(0, 0%, 100%, 0.4);
  border-radius: 50%;
  width: 80%;
  height: 80%;
  opacity: 0;
  -webkit-animation: ripple 2s 0.4s infinite;
  animation: ripple 2s 0.4s infinite;
}

body {
  background-color: black;
  opacity: 0.4;
}

@-webkit-keyframes init1 {
  20% {
    transform: scale(1.2);
  }

  40% {
    transform: scale(1.2);
  }

  60% {
    transform: scale(1);
  }
}

@keyframes init1 {
  20% {
    transform: scale(1.2);
  }

  40% {
    transform: scale(1.2);
  }

  60% {
    transform: scale(1);
  }
}

@-webkit-keyframes ripple {
  0% {
    opacity: 0;
    transform: translate(-50%, -50%);
  }

  1% {
    opacity: 1;
    transform: translate(-50%, -50%);
  }

  40% {
    transform: translate(-50%, -50%) scale(2);
    opacity: 0;
  }

  to {
    transform: translate(-50%, -50%) scale(2);
    opacity: 0;
  }
}

@keyframes ripple {
  0% {
    opacity: 0;
    transform: translate(-50%, -50%);
  }

  1% {
    opacity: 1;
    transform: translate(-50%, -50%);
  }

  40% {
    transform: translate(-50%, -50%) scale(2);
    opacity: 0;
  }

  to {
    transform: translate(-50%, -50%) scale(2);
    opacity: 0;
  }
}
</style>
