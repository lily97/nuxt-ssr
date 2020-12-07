<template>
  <div class="box">
    <div class="block-1">
      <div class="safe-area">
        <div class="production">
          <div class="introduce">
            <div class="title">
              <p class="big-title">战略合作</p>
              <p class="small-title">Strategic cooperation</p>
            </div>
            <div class="details">
              <p>
                智慧云已实际数据采集与处理为基础，利用物联网，大数据，云计算等技术
              </p>
              <p>以智能化为引领、信息化为支撑、网格化管理为基础</p>
              <p>解决“连得上、看得见、打得通”的解决方案</p>
            </div>
          </div>
          <div class="echarts"></div>
        </div>
      </div>
    </div>
    <div class="block-2">
      <div class="safe-area">
        <div class="advantage">
          <p class="adv-title">产品优势</p>
          <div class="bottom-line"></div>
          <div class="adv-content">
            <div class="adv-img"></div>
            <div class="adv-details">
              <p align="left">业务 + 数据 + 技术 + 设计</p>
              <p align="left">
                丰富的业务+海量数据+前沿web端技术+创新多维设计，共同打造出智慧云可视
                化，感受大数据的心跳，清晰有效传达数据背后业务的蓬勃发展
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="block-3">
      <div class="safe-area">
        <div class="solve">
          <p class="solve-title">解决行业痛点</p>
          <p class="min-title">
            高人力成本，数据读取错误，浪费资源，杂乱无章，效率低下等，这些经常出现的痛点，智慧云都能轻松解决
          </p>
          <div class="solve-info">
            <div class="center"></div>
            <div class="func-1">
              <div class="introduce">
                <p class="intr-title" align="left">实时数据</p>
                <p class="intr-details" align="left">实时查看电力数据</p>
              </div>
            </div>
            <div class="func-2">
              <div class="introduce">
                <p class="intr-title" align="left">电能质量监测</p>
                <p class="intr-details" align="left">排查电能质量，节省费用</p>
              </div>
            </div>
            <div class="func-3">
              <div class="introduce">
                <p class="intr-title" align="left">人力成本</p>
                <p class="intr-details" align="left">
                  智慧运维，解决人工费力成本
                </p>
              </div>
            </div>

            <div class="func-4">
              <div class="introduce">
                <p class="intr-title" align="left">智慧操作</p>
                <p class="intr-details" align="left">无人配电室，数据监控</p>
              </div>
            </div>

            <div class="func-5">
              <div class="introduce">
                <p class="intr-title" align="left">节约运营成本</p>
                <p class="intr-details" align="left">故障解析，提前维护</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="block-4">
      <div class="safe-area">
        <div class="cooperation">
          <p class="cooper-title">合作标准</p>
          <div class="cooper-content">
            <div
              class="card"
              @click="selCard = 0"
              :class="selCard == 0 ? 'sel-card' : ''"
            >
              <div class="cart-content">
                <i class="iconfont icon-authentic"></i>
                <div class="card-title">加盟资质</div>
                <div class="line"></div>
                <p align="left" class="card-details">
                  具有承装（修，试）电力设施许可证的电力
                  工程公司，电力设备公司等
                </p>
              </div>
              <div class="cart-line"></div>
            </div>
            <div
              class="card"
              @click="selCard = 1"
              :class="selCard == 1 ? 'sel-card' : ''"
            >
              <div class="cart-content">
                <i class="iconfont icon-repair"></i>
                <div class="card-title">个人资源</div>
                <div class="line"></div>
                <p align="left" class="card-details">
                  具有的供电企业资源，客户资源，电气公司
                  原电力工程公司，电力系统从业者
                </p>
              </div>
              <div class="cart-line"></div>
            </div>
            <div
              class="card"
              @click="selCard = 2"
              :class="selCard == 2 ? 'sel-card' : ''"
            >
              <div class="cart-content">
                <i class="iconfont icon-area"></i>
                <div class="card-title">地域要求</div>
                <div class="line"></div>
                <p align="left" class="card-details">
                  一线，二线，三线城市有电力行业，物业行
                  业，消防公司，工程，智慧园等场景应用。
                </p>
              </div>
              <div class="cart-line"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import $ from 'jquery'
export default {
  components: {},
  data() {
    return {
      scrollTop: 0,
      activeName: '0',
      imgList: [
        { url: '/img/transtion.png' },
        { url: '/img/transtion-details.png' },
        { url: '/img/transtion.png' },
        { url: '/img/transtion.png' },
      ],
      selCard: 0,
    }
  },
  mounted() {
    $('#footer').css('display', 'block')
    $('#header').css('position', 'fixed')
    $(window).scroll(function () {
      var top = $(document).scrollTop()
      this.scrollTop = top
      if (top > 590) {
        $('.link-a ').css('color', '#333333')
        $('#header').css({
          'background-color': '#ffffff',
          'box-shadow': '-20px 0px 10px 3px rgba(12, 16, 27, 0.06)',
        })
        $('#logo').attr('src', '/img/logo-green.png')
        $('.login').css('color', '#ffffff')
        $('.login').css('background', '#085e68')
      } else {
        $('.link-a ').css('color', '#ffffff')
          $('#header').css({
            'background-color': '',
            'box-shadow': '',
          })
        $('#logo').attr('src', '/img/logo.png')
        $('.login').css('color', '#085e68')
        $('.login').css('background', '#ffffff')
      }
    })
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event)
    },
  },
}
</script>

<style lang="scss" >
// 轮播样式
</style>

<style  lang="scss" scoped>
@import '~@/assets/style/mixin.scss';

// 1200像素安全区域
.safe-area {
  display: flex;
  justify-content: center;
  width: 1200px;
}

.box {
  height: auto;
  background: url('/img/cooperation.jpg') no-repeat;
  .block-1 {
    display: flex;
    justify-content: center;
    height: 620px;
    .production {
      width: 1100px;
      @include flex();
      .introduce {
        width: 1100px;
        color: #ffffff;
        .title {
          .big-title {
            width: 204px;
            height: 41px;
            font-size: 40px;
            font-weight: bold;
          }
          .small-title {
            margin-top: 15px;
            font-size: 20px;
            font-weight: bold;
            color: #ffffff;
          }
        }
        .details {
          margin-top: 60px;
          p {
            line-height: 35px;
          }
        }
      }
      .echarts {
        @include bgImg(848px, 456px, '/img/adv-6.png');
      }
    }
  }
  .block-2 {
    display: flex;
    justify-content: center;
    height: 728px;
    .advantage {
      width: 1100px;
      margin-top: 102px;
      text-align: center;
      .adv-title {
        font-size: 40px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #202020;
      }
      .bottom-line {
        margin: 0 auto;
        width: 40px;
        height: 5px;
        background: #085e68;
        margin-top: 5px;
      }
      .adv-content {
        @include flex();
        margin-top: 60px;
        .adv-img {
          @include bgImg(542px, 424px, '/img/two-person.png');
        }
        .adv-details {
          width: 503px;
          height: 208px;
          font-weight: bold;
          font-family: Microsoft YaHei;
          :first-child {
            font-size: 40px;
          }
          :last-child {
            margin-top: 30px;
            font-size: 14px;
          }

          font-size: 40px;
          color: #202020;
        }
      }
    }
  }
  .block-3 {
    display: flex;
    justify-content: center;
    height: 875px;
    background: url('/img/pain-points_bg.jpg') no-repeat;
    .solve {
      width: 1100px;
      margin-top: 79px;
      text-align: center;
      .solve-title {
        font-size: 40px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #202020;
      }
      .min-title {
        margin-top: 21px;
        font-size: 14px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #999999;
      }
      .solve-info {
        height: 620px;
        position: relative;
        display: flex;
        justify-content: center;
        div {
          width: 200;
          position: absolute;
        }
        .func-1,
        .func-2,
        .func-3,
        .func-4,
        .func-5 {
          .introduce {
            margin-left: 110%;
            margin-top: 45%;
            width: 119px;
            .intr-title {
              font-size: 18px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #666666;
            }
            .intr-details {
              font-size: 14px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #999999;
            }
          }
        }
        .center {
          margin-top: 150px;
          @include bgImg(683px, 401px, '/img/point.png', auto);
        }
        .func-1 {
          margin-right: 57%;
          margin-top: 8%;
          @include bgImg(92px, 92px, '/img/function-1.png', auto);
          .introduce {
            margin-left: 110%;
            margin-top: 45%;
            width: 119px;
          }
        }
        .func-2 {
          margin-right: 67%;
          margin-top: 39%;
          @include bgImg(113px, 140px, '/img/function-2.png', auto);
          .introduce {
            margin-left: 92%;
            margin-top: 45%;
            width: 165px;
          }
        }
        .func-3 {
          margin-left: 26%;
          margin-top: 5%;
          @include bgImg(140px, 101px, '/img/function-3.png', auto);
          .introduce {
            margin-left: 110%;
            margin-top: 5%;
            width: 195px;
          }
        }
        .func-4 {
          margin-left: 70%;
          margin-top: 15%;
          @include bgImg(92px, 92px, '/img/function-4.png', auto);
          .introduce {
            margin-left: 110%;
            margin-top: 45%;
            width: 150px;
          }
        }
        .func-5 {
          margin-left: 52%;
          margin-top: 31%;
          @include bgImg(102px, 130px, '/img/function-5.png', auto);
          .introduce {
            margin-left: 110%;
            margin-top: 45%;
            width: 134px;
          }
        }
      }
    }
  }
  .block-4 {
    display: flex;
    justify-content: center;
    height: 580px;
    .cooperation {
      text-align: center;
      width: 1110px;
      margin-top: 80px;
      .cooper-title {
        font-size: 40px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #202020;
      }
      .cooper-content {
        @include flex();
        margin-top: 120px;
        .iconfont {
          font-size: 30px;
          color: #085e68;
        }
        .card {
          width: 330px;
          height: 190px;
          background: #f8f8f8;
          border-radius: 10px;
          cursor: pointer;
          .cart-content {
            height: 182px;
            margin-top: 17px;
            .card-title {
              margin-top: 16px;
              font-size: 18px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #202020;
            }
            .line {
              margin-top: 13px;
              border-bottom: 1px solid #e2e2e2;
            }
            .card-details {
              width: 272px;
              font-size: 14px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #999999;
              line-height: 20px;
              margin: 18px auto;
            }
          }
        }
        .sel-card {
          background: #085e68;
          .iconfont {
            color: #ffffff;
          }
          .card-title {
            color: #ffffff !important;
          }
          .line {
            color: #0d707c !important;
          }
          .card-details {
            color: #b3d5d9 !important;
          }
          .cart-line {
            height: 6px;
            background: #0d5265;
            border-radius: 2px;
          }
        }
      }
    }
  }
}
</style>
