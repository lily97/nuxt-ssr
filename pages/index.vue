<template>
  <div class="box">
    <div class="nav" style="top: 0">
      <section class="block-1">
        <div class="title">
          <div class="big-title">智慧电力综合平台</div>
          <div class="line"></div>
          <div class="consulting">
            <div>我要了解 > ></div>
            <div>立即咨询 > ></div>
          </div>
        </div>
        <div class="baber">
          <Barrage :arr="arr" :isPause="isPause" :percent="100" />
        </div>
      </section>
      <section class="block-2">
        <div class="plan">
          <div class="solution">
            <div class="solu-1">解决方案</div>
            <div class="solu-2">Solution</div>
          </div>
          <div class="describe">
            <div class="left-bar">
              <div class="left-bar-1 dis-flex">
                <div class="iconfont icon-monitor"></div>
                <div class="align-left">
                  <span class="des-name">配电室智能监控</span>
                  <span class="des-content des-1">
                    全面云端化监测电气设备的数据，随时随地
                    掌握安全运行，防患于未然</span
                  >
                </div>
              </div>
              <div class="left-bar-2 dis-flex">
                <div class="iconfont icon-screening"></div>
                <div class="align-left">
                  <span class="des-name">故障排查，抢修</span>
                  <span class="des-content des-2">
                    基于能效大数据分析排查，实时监控
                    设备故障越限情况，进行快速到场 抢修，省时省力
                  </span>
                </div>
              </div>
              <div class="left-bar-3 dis-flex">
                <div class="iconfont icon-kanban"></div>
                <div class="align-left">
                  <span class="des-name">综合能效看板</span>
                  <span class="des-content des-3">
                    收集电气设备数据，对用电环比，电气监测，负荷，三相不平衡
                    变压器损耗，动态分析等以及用电回路和用能设备的能效情况，
                    便于查看采取措施
                  </span>
                </div>
              </div>
            </div>
            <div class="center-img"></div>
            <div class="right-bar">
              <div class="right-bar-1 dis-flex">
                <div class="iconfont icon-warning"></div>
                <div class="align-left">
                  <span class="des-name">设备报警诊断</span>
                  <span class="des-content des-4">
                    通过预警值以及温湿度采集仪等智能
                    设备，对设备进行实时安全监测
                  </span>
                </div>
              </div>
              <div class="right-bar-2 dis-flex">
                <div class="iconfont icon-data1"></div>
                <div class="align-left">
                  <span class="des-name">电能管理</span>
                  <span class="des-content des-5">
                    收集电气设备数据，对用电环比，电气监
                    测，负荷，三相不平衡变压器损耗，动态
                    分析等以及用电回路和用能设备的能效情 况，便于查看采取措施
                  </span>
                </div>
              </div>
              <div class="right-bar-3 dis-flex">
                <div class="iconfont icon-operate1"></div>
                <div class="align-left">
                  <span class="des-name">运维计划管理</span>
                  <span class="des-content des-6">
                    基于实时状态监控，实现无人值守，设备
                    云端存储提前预警，线上线下实现设备周 期的运维管理
                  </span>
                </div>
              </div>
            </div>
          </div>
          <div class="more">查看更多</div>
        </div>
      </section>
      <section class="block-3">
        <div class="scene">
          <div class="application">
            <div class="solu-1">应用场景</div>
            <div class="solu-2">Application scenario</div>
          </div>
          <div class="full-area">
            <div class="white-bg"></div>
            <div class="area-1200">
              <div class="list-bar">
                <div class="title">产品生态圈</div>
                <div class="table">
                  <div class="selected">办公建筑</div>
                  <div>商业建筑</div>
                  <div>科教文化建筑</div>
                  <div>体育,会展</div>
                  <div>通信建筑</div>
                  <div>新能源建筑</div>
                </div>
              </div>
              <div class="building"></div>
              <div class="apparatus"></div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>
<script>
import $ from 'jquery'
import Barrage from '@/components/Barrage'

export default {
  components: {
    Barrage,
  },
  data() {
    return {
      arr: [],
      isPause: false,
      sendContent: null,
      isJs: false,
      direction: 'default',
    }
  },
  mounted() {
    var kai = true,
      i = 0
    var oUl = document.getElementsByClassName('nav')[1]
    var footer = document.getElementById('footer')
    document.addEventListener('mousewheel', function (ev) {
      var ev = window.event || ev
      if (kai) {
        kai = false
        oUl.style.transition = ' 0.5s ease'
        if (ev.wheelDelta < 0 && i < 2) {
          i++
        }

        if (ev.wheelDelta > 0 && i > 0) {
          if (i == 2 && window.pageYOffset == 0) {
            i--
          } else if (ev.wheelDelta > 0 && i > 0 && i != 2) {
            i--
          }
        }
        console.log(i)
        if (i >= 2) {
          footer.style = 'display:block'
          $('.link-a ').css('color', '#333333')
          $('#header').css({
            'background-color': '#ffffff',
            'box-shadow': '-20px 0px 10px 3px rgba(12, 16, 27, 0.06)',
          })
          $('#header').css('position', 'fixed')
          $('#logo').attr('src', '/img/logo-green.png')
          $('.login').css('color', '#ffffff')
          $('.login').css('background', '#085e68')
        } else {
          footer.style = 'display:none'
          $('#header').css('position', 'absolute')
          $('.link-a ').css('color', '#ffffff')
          $('#header').css({
            'background-color': '',
            'box-shadow': '',
          })
          $('#logo').attr('src', '/img/logo.png')
          $('.login').css('color', '#085e68')
          $('.login').css('background', '#ffffff')
        }

        setTimeout(function () {
          oUl.style.top = -i * 100 + 'vh'
        }, 0)
        setTimeout(function () {
          kai = true
        }, 500)
      }
    })
    onresize
    window.onresize = function () {
      oUl.style.transition = 'none'
    }
    this.initTestData()
  },
  methods: {
    // 初始化模拟弹幕数据
    initTestData() {
      let arr = [
        '电力数据可视化平台',
        '故障报警',
        '智能网关',
        '能耗分析',
        '智能电力互联网',
        '用电管理',
        '资产管理',
      ]
      for (let i = 0; i < 6; i++) {
        for (let index = 0; index < 1000; index++) {
          if (index % 2 == 0) {
            this.arr.push({
              direction: 'top',
              content: arr[parseInt(Math.random() * arr.length)],
            })
          } else {
            this.arr.push({
              direction: 'default',
              content: arr[parseInt(Math.random() * arr.length)],
            })
          }
        }
      }
    },
  },
}
</script>

<style  lang="scss" scoped>
@import '~@/assets/style/mixin.scss';
.box {
  .nav {
    .block-1 {
      position: relative;
      @include flex();
      width: 100%;
      background: url('/img/banner.png') no-repeat;
      background-color: #1f2c41;
      .title {
        width: 600px;
        position: absolute;
        @include flex();
        right: 12%;
        top: 26%;
        .big-title {
          font-size: 60px;
          font-weight: bold;
          color: #ffffff;
          text-shadow: 0px 2px 26px rgba(21, 32, 50, 0.24);
        }
        .line {
          width: 1px;
          height: 56px;
          background: #334767;
        }
        .consulting {
          font-size: 14px;
          font-weight: bold;
          color: #adb1b9;
          cursor: pointer;
        }
      }
      .baber {
        height: 722px;
        width: 600px;
        position: absolute;
        top: 45%;
        right: 0;
      }
    }
    .block-2 {
      width: 100%;
      background: url('/img/plan.png') no-repeat;
      .plan {
        min-width: 1200px;
        width: 1200px;
        margin: 36px auto 0 auto;
        margin-top: 95px;
        .solution {
          .solu-1 {
            font-size: 40px;
            font-weight: bold;
            color: #ffffff;
          }
          .solu-2 {
            margin-top: 17px;
            font-size: 24px;
            font-weight: bold;
            color: #ffffff;
          }
        }
        .describe {
          margin-top: 8%;
          @include flex();
          .iconfont {
            color: rgb(129, 138, 153);
            font-size: 30px;
            line-height: 30px;
          }
          .left-bar {
            .left-bar-2 {
              margin-top: 18%;
            }
            .left-bar-3 {
              margin-top: 18%;
            }
          }
          .right-bar {
            .right-bar-1 {
              margin-bottom: 28%;
            }
            .right-bar-2 {
              margin-top: 18%;
            }
            .right-bar-3 {
              margin-top: 18%;
            }
          }
          .dis-flex {
            display: flex;
          }
          .align-left {
            margin-left: 13px;
            text-align: left;
          }
          span {
            display: block;
          }
          .des-name {
            font-size: 20px;
            font-weight: bold;
            color: #bec6d2;
          }
          .des-content {
            font-size: 14px;
            font-weight: bold;
            color: #818a99;
          }
          .des-1 {
            margin-top: 15px;
            width: 273px;
          }
          .des-2 {
            margin-top: 15px;
            width: 230px;
          }
          .des-3 {
            margin-top: 15px;
            width: 403px;
          }
          .des-4 {
            margin-top: 15px;
            width: 230px;
          }
          .des-5 {
            margin-top: 15px;
            width: 260px;
          }
          .des-6 {
            margin-top: 15px;
            width: 259px;
          }
        }
        .more {
          margin-top: 10%;
          float: right;
          cursor: pointer;
          width: 100px;
          height: 30px;
          background: #343d47;
          border-radius: 15px;
          line-height: 30px;
          font-size: 14px;
          color: #bec6d2;
        }
      }
    }
    .block-3 {
      width: 100%;
      background: url('/img/scene.png') no-repeat;
      justify-content: center;
      .scene {
        // min-width: 1200px;
        width: 100%;
        // margin: 36px auto 0 auto;
        margin-top: 95px;
        .application {
          .solu-1 {
            font-size: 40px;
            font-weight: bold;
            color: #ffffff;
          }
          .solu-2 {
            margin-top: 17px;
            font-size: 24px;
            font-weight: bold;
            color: #ffffff;
          }
        }
        .full-area {
          margin-top: 100px;
          position: relative;
          .white-bg {
            width: 60%;
            height: 480px;
            background: #ffffff;
            border-radius: 10px;
          }
          .area-1200 {
            width: 1200px;
            min-width: 1200px;
            height: 360px;
            position: absolute;
            top: 10%;
            background: #945151;
            left: 19.5%;
            display: flex;
            .list-bar {
              width: 150px;
              height: 355px;
              border: 5px solid #085e68;
              .title {
                margin-top: 20px;
                font-size: 20px;
                font-weight: bold;
                color: #202020;
              }
              .table {
                margin-top: 30px;
                .selected {
                  color: #ffffff;
                  background-image: linear-gradient(to right, #085e68, #10c0d3);
                }
                div {
                  height: 30px;
                  margin-bottom: 5px;
                  font-size: 14px;
                  font-weight: bold;
                  color: #202020;
                  line-height: 30px;
                }
              }
            }
            .building {
              position: relative;
              left: -2%;
              top: 20%;
              @include bgImg(500px, 220px, '/img/buildings.png', auto);
            }
            .apparatus {
              position: relative;
              left: -4%;
              top: 13%;
              @include bgImg(350px, 250px, '/img/apparatus.png');
            }
          }
        }
      }
    }
  }
}
</style>

<style type="text/css">
.nav {
  position: relative;
}

section {
  width: 100%;
  height: 100vh;
  font-size: 30px;
  position: relative;
  display: flex;
  text-align: center;
}
</style>