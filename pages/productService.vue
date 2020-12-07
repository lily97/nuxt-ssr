<template>
  <div class="box">
    <div class="block-1">
      <div class="safe-area">
        <div class="production">
          <div class="introduce">
            <div class="title">
              <p class="big-title">产品与服务</p>
              <p class="small-title">Products and services</p>
            </div>
            <div class="details">
              <p>
                领先的大数据监控技术、成熟的智慧电力能效管理解决方案助力企业智慧电力物联网升级
              </p>
              <p>智慧式用电安全隐患监控服务系统</p>
              <p>智慧电力数据检测平台</p>
              <p>智慧电力运维服务云平台</p>
            </div>
          </div>
          <div class="echarts"></div>
        </div>
      </div>
    </div>
    <div class="block-2" :class="scrollTop > 590 ? 'pos-fix' : ''">
      <div class="safe-area">
        <div class="use-bar">
          <div @click="clickBar(0, 450)" :class="selBar == 0 ? 'selected' : ''">
            产品概述
          </div>
          <div @click="clickBar(1, 838)" :class="selBar == 1 ? 'selected' : ''">
            功能概括
          </div>
          <div
            @click="clickBar(2, 3166)"
            :class="selBar == 2 ? 'selected' : ''"
          >
            系统架构
          </div>
          <div
            @click="clickBar(3, 4217)"
            :class="selBar == 3 ? 'selected' : ''"
          >
            产品特点
          </div>
        </div>
      </div>
    </div>
    <div class="block-3">
      <div class="safe-area">
        <div class="describe">
          <p class="desc-title">产品概述</p>
          <p class="desc-details" align="left">
            智慧云平台是基于移动物联网，大数据，云计算技术，通过物联网创新应用，将漏电，温度，湿度，电流，电压等安全数据实时传送至平台，实现不间断
            的数据跟踪与统计分析和管理，智慧云对于电能质量可在线实时监测变电站，电厂电网的三相电压，三相电流，和谐波等相关电力数据监测，降低电能损
            耗，保障电能可靠，经济运行
          </p>
        </div>
      </div>
    </div>
    <div class="block-4">
      <div class="safe-area">
        <div class="function">
          <div class="view-1">
            <p class="func-title">功能概括</p>
            <div class="func-bar">
              <el-tabs v-model="activeName" @tab-click="handleClick">
                <el-tab-pane label="综合能耗看板" name="0" topScoll="840">
                </el-tab-pane>
                <el-tab-pane label="电能/负荷采集监控" name="1" topScoll="1485">
                </el-tab-pane>
                <el-tab-pane label="智慧用电安全监控" name="2" topScoll="1823">
                </el-tab-pane>
                <el-tab-pane label="远程故障管理" name="3" topScoll="2131">
                </el-tab-pane>
                <el-tab-pane label="智慧运维" name="4" topScoll="2523">
                </el-tab-pane>
                <el-tab-pane label="设备云管理" name="5" topScoll="2885">
                </el-tab-pane>
              </el-tabs>
            </div>
          </div>

          <div class="view-3">
            <div class="kanban-details">
              <div class="kb-title">
                <div class="bold-line"></div>
                <div>综合能耗看板</div>
              </div>
              <div class="kb-desc">
                基于实时状态监测，实现配电室的无人值守；实现档案的云端
                化存储及查询，管理，故障检修，隐患保修，派工，交接班，
                以及统计开关分合次数及设备投运时间，实现设备全生命周期
                的运维管理
              </div>
              <div class="explain-bar">
                <div class="bars">
                  <div class="circle circle-1"></div>
                  <div>故障分级报警</div>
                </div>
                <div class="bars">
                  <div class="circle circle-2"></div>
                  <div>电力数据采集</div>
                </div>
                <div class="bars">
                  <div class="circle circle-3"></div>
                  <div>数据可视化</div>
                </div>
                <div class="bars">
                  <div class="circle circle-4"></div>
                  <div>用电能效分析</div>
                </div>
                <div class="bars">
                  <div class="circle circle-5"></div>
                  <div>大数据智慧对比</div>
                </div>
              </div>
            </div>
            <div class="kanban-img">
              <div class="img-title">综合能效看板</div>
              <div class="kb-img"></div>
            </div>
          </div>
          <div class="lightning">
            <div>
              <i
                class="iconfont icon-shandian"
                style="width: 18px; height: 30px"
              ></i>
            </div>
            <div class="dot-line"></div>
          </div>
          <div class="view-4">
            <div class="person"></div>
            <div class="kanban-details">
              <div class="kb-title">
                <div class="bold-line"></div>
                <div>电能/负荷采集监控</div>
              </div>
              <div class="kb-desc">
                通过智能电力监控仪表将数据上传到云平台，
                自动实现电能消耗的周月季年统计报表，
                并对电能消耗作好同比、环比分析，
                及时发现用电黑洞，从管理上节能，
                研究消除供配电系统中的无功补偿和谐波治理问题电能质量问题提供合适的设计解决方案，
                以达到改善供电质量和确保电力系统安全经济运行的目的。
              </div>
            </div>
          </div>
          <div class="lightning">
            <div class="dot-line"></div>
            <div>
              <i
                class="iconfont icon-shandian"
                style="width: 18px; height: 30px"
              ></i>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 智慧用电安全 start -->
    <div class="block-5">
      <div class="safe-area">
        <div class="security-power">
          <div class="view-1">
            <div class="kanban-details">
              <div class="kb-title">
                <div class="bold-line"></div>
                <div>智慧用电安全</div>
              </div>
              <div class="kb-desc">
                实时发电电气线路和用电设备所存在的安全隐患(如线缆温度异常)
                漏电流越限，过流，过压，欠压等），及时发送预警信息，实现
                “防患于未然”的目的
              </div>
            </div>
          </div>
          <div class="view-2"></div>
        </div>
      </div>
      <div class="lightning">
        <div>
          <i
            class="iconfont icon-shandian"
            style="width: 18px; height: 30px"
          ></i>
        </div>
        <div class="dot-line"></div>
      </div>
    </div>
    <!-- 智慧用电安全 end -->

    <!-- 远程故障管理 start -->
    <div class="block-6">
      <div class="safe-area">
        <div class="security-power">
          <div class="view-2"></div>
          <div class="view-1">
            <div class="kanban-details">
              <div class="kb-title">
                <div class="bold-line"></div>
                <div>远程故障管理</div>
              </div>
              <div class="kb-desc">
                当平台收到报警或故障信息时，平台将以短信，电话或APP推送
                等方式通知管理人员，远程安排工作人员携带相应工具快速到现场维修，实现省时，省力，快速的运作模式
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="lightning">
        <div class="dot-line"></div>
        <div>
          <i
            class="iconfont icon-shandian"
            style="width: 18px; height: 30px"
          ></i>
        </div>
      </div>
    </div>
    <!-- 远程故障管理 end -->

    <!-- 智慧运维 start -->
    <div class="block-7">
      <div class="safe-area">
        <div class="security-power">
          <div class="view-1">
            <div class="kanban-details">
              <div class="kb-title">
                <div class="bold-line"></div>
                <div>智慧运维</div>
              </div>
              <div class="kb-desc">
                当平台收到报警或故障信息时，平台将以短信，电话或APP推送
                等方式通知管理人员，远程安排工作人员携带相应工具快速到现场维修，实现省时，省力，快速的运作模式
              </div>
            </div>
          </div>
          <div class="view-2"></div>
        </div>
      </div>
      <div class="lightning">
        <div>
          <i
            class="iconfont icon-shandian"
            style="width: 18px; height: 30px"
          ></i>
        </div>
        <div class="dot-line"></div>
      </div>
    </div>
    <!-- 智慧运维 end -->

    <!-- 设备云管理 start -->
    <div class="block-8">
      <div class="safe-area">
        <div class="security-power">
          <div class="view-2">
            <el-carousel
              :interval="4000000"
              type="card"
              height="475px"
              indicator-position="none"
            >
              <el-carousel-item v-for="(item, index) in imgList" :key="index">
                <img
                  :src="item.url"
                  alt=""
                  style="width: 262px; height: 475px"
                />
              </el-carousel-item>
            </el-carousel>
          </div>
          <div class="view-1">
            <div class="kanban-details">
              <div class="kb-title">
                <div class="bold-line"></div>
                <div>设备云管理</div>
              </div>
              <div class="kb-desc">
                实现云监测电力数据，设备健康指数评级，
                设备开启与关闭等功能，实时对数据进行监测浏览与异常情况，
                远程智能操作设备状态（开门，与关门）等操作以及设备数据编辑与设置，
                实现省时省力更省心。
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 设备云管理 end -->

    <!-- 产品架构 start -->
    <div class="block-9">
      <div class="safe-area">
        <div class="product">
          <div class="product-title">产品架构</div>
          <div class="content">
            <div class="left-con">
              <div class="kanban-details">
                <div class="kb-title">
                  <div class="bold-line"></div>
                  <div>客户应用层</div>
                </div>
                <div class="kb-desc">
                  应用层提供友好的人机界面，用户可通过
                  PC端查询用电数据、设备状态、环境等信
                  息，同时可对设备资产、运维工单、图纸 资料进行管理
                </div>
              </div>
              <div class="kanban-details">
                <div class="kb-title">
                  <div class="bold-line"></div>
                  <div>设备采集层</div>
                </div>
                <div class="kb-desc">
                  设备采集层是系统的最底层也是系统
                  的基础，系统所有基础数据及信息均
                  来自该层。该层设备由具有通讯接口 的智能设备组成
                </div>
              </div>
            </div>
            <div class="middle-con"></div>
            <div class="right-con">
              <div class="kanban-details bottom-30">
                <div class="kb-title">
                  <div class="bold-line"></div>
                  <div>智慧云云端</div>
                </div>
                <div class="kb-desc">
                  云端是系统核心组成部分，完成海量基础
                  数据集中解析处理、存储、分析， 是客户
                  应用层与设备采集层的中间连接部分
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 产品架构 end -->

    <!-- 产品特点 start -->
    <div class="block-10">
      <div class="trait">
        <div class="trait-title">产品特点</div>
        <!-- <div class="card"> -->
        <div class="safe-area">
          <div class="left-card"></div>
          <div class="right-card">
            <div class="card-content">
              <div class="card-title">智慧运维</div>
              <div class="card-lsit">
                <div class="list">
                  <div class="circle"></div>
                  <div>实现运维效率高</div>
                </div>
                <div class="list">
                  <div class="circle"></div>
                  <div>响应快</div>
                </div>
                <div class="list">
                  <div class="circle"></div>
                  <div>运维过程标准规范</div>
                </div>
                <div class="list">
                  <div class="circle"></div>
                  <div>巡检过程便于监管</div>
                </div>
                <div class="list">
                  <div class="circle"></div>
                  <div>设备档案管理</div>
                </div>
                <div class="list">
                  <div class="circle"></div>
                  <div>运行大数据分析</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- </div> -->
      </div>
    </div>
    <!-- 产品特点 end -->
  </div>
</template>


<script>
import $ from 'jquery'
export default {
  components: {},
  data() {
    return {
      selBar: -1,
      scrollTop: 0,
      activeName: '0',
      index: 0,
      imgList: [
        { url: '/img/phone-1.jpg' },
        { url: '/img/phone-2.jpg' },
        { url: '/img/phone-3.jpg' },
      ],
    }
  },
  mounted() {
    $('#footer').css('display', 'block')
    $('#header').css('position', 'fixed')

    $(window).scroll(function () {
      var top = $(document).scrollTop()
      this.scrollTop = top
      if (top >= 438) {
        $('.link-a ').css('color', '#333333')
        $('#header').css('background-color', '#ffffff')
        $('#logo').attr('src', '/img/logo-green.png')
        $('.login').css('color', '#ffffff')
        $('.login').css('background', '#085e68')
        $('.block-2').css({
          position: 'fixed',
          top: '80px',
          width: '100%',
          background: '#333333',
        })
        $('.block-3').css('margin-top', '100px')
      } else {
        $('.link-a ').css('color', '#ffffff')
        $('#header').css({
          'background-color': '',
          'box-shadow': '',
        })
        $('#logo').attr('src', '/img/logo.png')
        $('.login').css('color', '#085e68')
        $('.login').css('background', '#ffffff')
        $('.block-2').css({ position: '', top: '', width: '', background: '' })
        $('.block-3').css('margin-top', '')
      }
    })
  },
  methods: {
    clickBar(index, top) {
      this.selBar = index
      $(document).scrollTop(top)
    },
    handleClick(tab, event) {
      var top = Number(tab.$attrs.topScoll)
      $(document).scrollTop(top)
    },
  },
}
</script>

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
  background: url('/img/product.jpg') no-repeat;
  .block-1 {
    display: flex;
    justify-content: center;
    margin: 150px auto 0 auto;
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
        @include bgImg(592px, 375px, '/img/echarts.png');
      }
    }
  }
  .block-2 {
    height: 90px;
    background: rgba($color: #110f0f, $alpha: 0.36);
    display: flex;
    justify-content: center;
    z-index: 9999;
    .pos-fix {
      position: fixed;
      width: 100%;
      top: 80px;
      background: #333333;
    }
    .use-bar {
      width: 1000px;
      @include flex();
      .selected {
        color: #085e68;
      }
      div {
        cursor: pointer;
        height: 14px;
        font-size: 14px;
        font-weight: bold;
        color: #ffffff;
      }
    }
  }
  .block-3 {
    display: flex;
    justify-content: center;
    height: 381px;
    .describe {
      width: 900px;
      text-align: center;
      color: #202020;
      font-weight: bold;
      .desc-title {
        margin-top: 80px;
        font-size: 40px;
      }
      .desc-details {
        margin-top: 80px;
        width: 963px;
        font-size: 14px;
        font-weight: bold;
      }
    }
  }
  .block-4 {
    display: flex;
    justify-content: center;
    height: 953px;
    background: url('/img/function.png') no-repeat;
    .function {
      width: 1140px;
      .view-1 {
        margin-top: 50px;
        text-align: center;
        .func-title {
          font-size: 40px;
          font-family: Microsoft YaHei;
          color: #202020;
          font-weight: bold;
        }
        .func-bar {
          margin-top: 40px;
        }
        // 深度穿透ele样式
        .func-bar::v-deep {
          .el-tabs__nav-scroll {
            display: flex;
            justify-content: center;
          }
          .el-tabs__nav-wrap::after {
            height: 1px;
            background: #e2e2e2;
          }
          .el-tabs__item {
            padding: 0 48px;
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #454b4c;
          }
          .el-tabs__item:hover {
            color: #085e68;
          }
          .el-tabs__item.is-active {
            color: #085e68;
          }
          .el-tabs__active-bar {
            background-color: #085e68;
            height: 4px;
          }
        }
      }

      .view-3 {
        margin-top: 30px;
        @include flex();
        .kanban-details {
          width: 389px;
          height: 400px;
          margin-left: 2%;
          .kb-title {
            margin-top: 100px;
            font-weight: bold;
            font-size: 20px;
            font-family: Microsoft YaHei;
            color: #202020;
            display: flex;
            .bold-line {
              margin-top: 4px;
              width: 3px;
              height: 20px;
              background: #085e68;
            }
            :last-child {
              margin-left: 10px;
            }
          }
          .kb-desc {
            margin-top: 25px;
            margin-left: 10px;
            font-weight: bold;
            font-size: 14px;
            font-family: Microsoft YaHei;
            color: #454b4c;
          }
          .explain-bar {
            display: flex;
            flex-wrap: wrap;
            margin-left: 10px;
            margin-top: 35px;
            .bars {
              width: 125px;
              height: 15px;
              font-size: 14px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #454b4c;
              margin-bottom: 20px;
              display: flex;
              align-items: center;
              .circle {
                width: 10px;
                height: 10px;
                border-radius: 50%;
                margin-right: 17px;
              }
              .circle-1 {
                background-color: #2fad58;
              }
              .circle-2 {
                background-color: #2097fd;
              }
              .circle-3 {
                background-color: #febc09;
              }
              .circle-4 {
                background-color: #f95649;
              }
              .circle-5 {
                background-color: #8e70fd;
              }
            }
          }
        }
        .kanban-img {
          width: 660px;
          height: 400px;
          background: url('/img/kb-bgImg.png') no-repeat;
          .img-title {
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #666666;
            text-align: center;
            margin-top: 20px;
          }
        }
      }
      .view-4 {
        display: flex;
        justify-content: space-between;
        margin-top: 30px;
        .person {
          @include bgImg(381px, 286px, '/img/person.png');
        }
        .kanban-details {
          width: 411px;
          margin-right: 5%;
          .kb-title {
            margin-top: 50px;
            font-weight: bold;
            font-size: 20px;
            font-family: Microsoft YaHei;
            color: #202020;
            display: flex;
            .bold-line {
              margin-top: 4px;
              width: 3px;
              height: 20px;
              background: #085e68;
            }
            :last-child {
              margin-left: 10px;
            }
          }
          .kb-desc {
            margin-top: 25px;
            margin-left: 10px;
            font-weight: bold;
            font-size: 14px;
            font-family: Microsoft YaHei;
            color: #454b4c;
          }
        }
      }
      .lightning {
        margin-top: 50px;
        margin: 0 auto;
        width: 1160px;
        display: flex;
        .dot-line {
          width: 1153px;
          border: 1px dotted #e2e2e2;
          height: 0px;
          margin-top: 17px;
        }
      }
    }
  }
  .block-5 {
    margin-top: 50px;
  }
  .block-5,
  .block-6,
  .block-7 {
    .safe-area {
      margin: 0 auto;
    }
    .security-power {
      width: 1100px;
      display: flex;
      justify-content: space-between;
      .view-1 {
        .kanban-details {
          width: 414px;
          margin-right: 5%;
          .kb-title {
            margin-top: 50px;
            font-weight: bold;
            font-size: 20px;
            font-family: Microsoft YaHei;
            color: #202020;
            display: flex;
            .bold-line {
              margin-top: 4px;
              width: 3px;
              height: 20px;
              background: #085e68;
            }
            :last-child {
              margin-left: 10px;
            }
          }
          .kb-desc {
            margin-top: 25px;
            margin-left: 10px;
            font-weight: bold;
            font-size: 14px;
            font-family: Microsoft YaHei;
            color: #454b4c;
          }
        }
      }
      .view-2 {
        @include bgImg(421px, 273px, '/img/product-service.png');
      }
    }
    .lightning {
      margin-top: 50px;
      margin: 0 auto;
      width: 1160px;
      display: flex;
      .dot-line {
        width: 1153px;
        border: 1px dotted #e2e2e2;
        height: 0px;
        margin-top: 17px;
      }
    }
  }
  .block-6 {
    margin-top: 80px;
    .security-power {
      .view-2 {
        @include bgImg(443px, 291px, '/img/working.png');
      }
    }
  }
  .block-7 {
    margin-top: 50px;
    .security-power {
      .view-2 {
        @include bgImg(443px, 291px, '/img/operation.png');
      }
    }
  }
  .block-8 {
    .safe-area {
      margin: 0 auto;
    }
    .security-power {
      width: 1160px;
      display: flex;
      justify-content: space-between;
      margin-top: 150px;
      .view-1 {
        .kanban-details {
          width: 414px;
          margin-right: 5%;
          .kb-title {
            margin-top: 50px;
            font-weight: bold;
            font-size: 20px;
            font-family: Microsoft YaHei;
            color: #202020;
            display: flex;
            .bold-line {
              margin-top: 4px;
              width: 3px;
              height: 20px;
              background: #085e68;
            }
            :last-child {
              margin-left: 10px;
            }
          }
          .kb-desc {
            margin-top: 25px;
            margin-left: 10px;
            font-weight: bold;
            font-size: 14px;
            font-family: Microsoft YaHei;
            color: #454b4c;
          }
        }
      }
      .view-2 {
        height: 475px;
        width: 600px;
      }
    }
  }
  .block-9 {
    background: url('/img/map-bg.png') no-repeat;
    height: 1054px;
    background-position: center;
    background-color: #f7f8fb;
    display: flex;
    justify-content: center;
    margin-top: 100px;
    .product {
      width: 1120px;
      margin-top: 50px;
      .product-title {
        font-size: 40px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #202020;
        text-align: center;
      }
      .content {
        margin-top: 90px;
        @include flex();
        .bottom-30 {
          margin-bottom: 30px;
        }
        .kanban-details {
          width: 264px;
          .kb-title {
            margin-top: 50px;
            font-weight: bold;
            font-size: 20px;
            font-family: Microsoft YaHei;
            color: #202020;
            display: flex;
            .bold-line {
              margin-top: 4px;
              width: 3px;
              height: 20px;
              background: #085e68;
            }
            :last-child {
              margin-left: 10px;
            }
          }
          .kb-desc {
            margin-top: 25px;
            margin-left: 10px;
            font-weight: bold;
            font-size: 14px;
            font-family: Microsoft YaHei;
            color: #454b4c;
          }
        }
        .left-con {
          height: 760px;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
        }
        .middle-con {
          margin-left: 2%;
          @include bgImg(508px, 760px, '/img/process.png');
        }
        .right-con {
          margin-bottom: 265px;
          .kanban-details {
            width: 267px;
          }
        }
      }
    }
  }
  .block-10 {
    background: url('/img/trait.jpg') no-repeat;
    height: 685px;
    display: flex;
    justify-content: center;
    .trait {
      margin-top: 50px;
      width: 100%;
      .trait-title {
        font-size: 40px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #202020;
        text-align: center;
      }
      .safe-area {
        width: 1600px;
        justify-content: flex-end;
        margin-top: 40px;
        float: right;
        .left-card {
          width: 200px;
          background-color: rosybrown;
        }
        .right-card {
          @include bgImg(980px, 399px, '/img/right-card.png');
          .card-content {
            margin-left: 100px;
            margin-top: 60px;
            .card-title {
              font-size: 28px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #ffffff;
            }
            .card-lsit {
              margin-top: 30px;
              .list {
                font-size: 16px;
                font-family: Microsoft YaHei;
                font-weight: bold;
                color: #ffffff;
                margin-bottom: 15px;
                display: flex;
                align-items: center;
                .circle {
                  width: 6px;
                  height: 6px;
                  background: #ffffff;
                  opacity: 0.41;
                  border-radius: 50%;
                  margin-right: 10px;
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>
