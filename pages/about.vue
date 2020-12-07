<template>
  <div class="box">
    <div class="block-1">
      <div class="safe-area">
        <div class="production">
          <div class="introduce">
            <p class="title-1">关于我们</p>
            <p class="title-2">About us</p>
            <p class="title-3">
              科技赋能产业，降低成本，提高效益，实现电力智慧运行
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="block-2">
      <div class="safe-area">
        <div class="advantage">
          <p class="adv-title">产品优势</p>
          <div class="bottom-line"></div>
          <div class="adv-content">
            <p class="details" align="left">
              智慧云隶属于郑州国源电力集团有限公司旗下产品，专注基于大数据分析，电子智能化，信息安全，电力自动化，等领域，
              利用先进的信息化手段和互联网+服务运营模式，产研结合，形成了以设计，软硬件产品，系统建设，
              工程建设，智能运维为核心的业务发展布局。
            </p>
            <p class="details" align="left">
              为智慧园区、智能楼宇、数字化企业、厂
              矿、公共事业单位、居民小区等110KV及以下电压等级的变电站、配电室等提供电
              力监控、数据可视化、预警报警、能耗优化和电气安全等专业化提供一体化的解决方案，
              为客户降低运行成本，帮助客户提升市场核心竞争力和利润最大化。
            </p>
            <p class="details" align="left">
              科技赋能产业，降低成本，提高效益，实现电力智慧运行、管理无人值守和远程智
              能服务，让智慧用电、安全用电获得全新体验，这里解决综合性问题，提高运行效率。
            </p>
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
    return {}
  },
  mounted() {
    $('#footer').css('display', 'block')
    $('#header').css('position', 'fixed')
    $(window).scroll(function () {
      var top = $(document).scrollTop()
      if (top >= 500) {
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
  background: url('/img/about-us.jpg') no-repeat;
  .block-1 {
    display: flex;
    justify-content: center;
    height: 620px;
    .production {
      width: 1100px;
      text-align: center;
      display: flex;
      align-items: center;
      .introduce {
        width: 1100px;
        color: #ffffff;
        .title-1 {
          font-size: 40px;
          font-family: Microsoft YaHei;
          font-weight: bold;
          color: #ffffff;
          text-shadow: 0px 2px 26px rgba(21, 32, 50, 0.24);
        }
        .title-2 {
          margin-top: 17px;
          font-size: 20px;
          font-family: Microsoft YaHei;
          font-weight: bold;
          color: #ffffff;
          text-shadow: 0px 2px 26px rgba(21, 32, 50, 0.24);
        }
        .title-3 {
          margin-top: 54px;
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: bold;
          color: #ffffff;
          text-shadow: 0px 2px 26px rgba(21, 32, 50, 0.24);
        }
      }
    }
  }
  .block-2 {
    display: flex;
    justify-content: center;
    height: 475px;
    .safe-area {
      margin-top: -90px;
      background-color: #ffffff;
      height: 701px;
      box-shadow: 0px -19px 47px 15px rgba(12, 16, 27, 0.06);
      border-radius: 20px;
    }
    .advantage {
      width: 1100px;
      margin-top: 90px;
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
        margin-top: 38px;
        .details {
          width: 1096px;
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: bold;
          color: #202020;
          margin-bottom: 50px;
        }
      }
    }
  }
}
</style>
