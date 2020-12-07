<template>
  <div class="box">
    <div class="block-1">
      <div class="safe-area">
        <div class="production">
          <div class="introduce">
            <div class="title">
              <p class="big-title">解决方案</p>
              <p class="small-title">Solution</p>
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
        <div class="describe">
          <p class="desc-title">方案概述</p>
          <div class="bottom-line"></div>
          <div class="desc-details">
            <div class="left-details">
              <div class="equipment"></div>
            </div>
            <div class="right-details">
              <div class="summary">
                <div class="sum-title">方案概述</div>
                <div class="sum-details">
                  <p align="left">
                    全面检测电力设备(高/低压配电柜，变压器，箱式变电站，配电箱等)的电力参数，运行参数，安全状态及环境数据，实时进行大数据的诊断分析及趋势预估
                  </p>
                  <p align="left">
                    越限预警，经现场统一与无线设备的连接，实现数据的综合采集与平台上传随时掌握设备安全运行状况，智能化安全监控与运维管理。
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="rotation">
            <el-carousel
              :interval="4000000"
              type="card"
              height="260px"
              indicator-position="none"
            >
              <el-carousel-item v-for="(item, index) in imgList" :key="index">
                <img :src="item.url" alt="" />
              </el-carousel-item>
            </el-carousel>
          </div>
        </div>
      </div>
    </div>
    <div class="block-3">
      <div class="safe-area">
        <div class="function">
          <div class="view-1">解决方案</div>
          <div class="view-2">
            <el-tabs v-model="activeName" @tab-click="handleClick" >
              <el-tab-pane label="配电室智能监控" name="0">
                <div class="rotation-7">
                  <div class="kanban-details">
                    <div class="kb-title">
                      <div class="bold-line"></div>
                      <div>配电室智能监控</div>
                    </div>
                    <div class="kb-desc">
                      实时全方位监视用户配电系统的运行状态和电量数据，提供
                      用户概括，电力数据监测，电能质量分析，用电分析，日/
                      月/年用能数据报表，异常事件报警和记录，运行，环境监测
                      运维管理等功能
                    </div>
                    <div class="scene">应用场景</div>
                    <div class="explain-bar">
                      <div class="bars bars-lang">
                        <div class="circle circle-1"></div>
                        <div>电力运行维护企业</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-2"></div>
                        <div>集团企业</div>
                      </div>
                      <div class="bars bars-middle">
                        <div class="circle circle-3"></div>
                        <div>院校主管单位</div>
                      </div>
                      <div class="bars bars-lang">
                        <div class="circle circle-4"></div>
                        <div>智慧社区</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-5"></div>
                        <div>工厂</div>
                      </div>
                    </div>
                  </div>
                  <div class="kanban-img"></div>
                </div>
              </el-tab-pane>
              <el-tab-pane label="配电设备报警" name="1">
                <div class="rotation-7">
                  <div class="kanban-details">
                    <div class="kb-title">
                      <div class="bold-line"></div>
                      <div>配电室智能监控11</div>
                    </div>
                    <div class="kb-desc">
                      实时全方位监视用户配电系统的运行状态和电量数据，提供
                      用户概括，电力数据监测，电能质量分析，用电分析，日/
                      月/年用能数据报表，异常事件报警和记录，运行，环境监测
                      运维管理等功能
                    </div>
                    <div class="scene">应用场景</div>
                    <div class="explain-bar">
                      <div class="bars bars-lang">
                        <div class="circle circle-1"></div>
                        <div>电力运行维护企业</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-2"></div>
                        <div>集团企业</div>
                      </div>
                      <div class="bars bars-middle">
                        <div class="circle circle-3"></div>
                        <div>院校主管单位</div>
                      </div>
                      <div class="bars bars-lang">
                        <div class="circle circle-4"></div>
                        <div>智慧社区</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-5"></div>
                        <div>工厂</div>
                      </div>
                    </div>
                  </div>
                  <div class="kanban-img"></div>
                </div>
              </el-tab-pane>
              <el-tab-pane label="配电设备缺陷消除" name="2">
                <div class="rotation-7">
                  <div class="kanban-details">
                    <div class="kb-title">
                      <div class="bold-line"></div>
                      <div>配电室智能监控11</div>
                    </div>
                    <div class="kb-desc">
                      实时全方位监视用户配电系统的运行状态和电量数据，提供
                      用户概括，电力数据监测，电能质量分析，用电分析，日/
                      月/年用能数据报表，异常事件报警和记录，运行，环境监测
                      运维管理等功能
                    </div>
                    <div class="scene">应用场景</div>
                    <div class="explain-bar">
                      <div class="bars bars-lang">
                        <div class="circle circle-1"></div>
                        <div>电力运行维护企业</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-2"></div>
                        <div>集团企业</div>
                      </div>
                      <div class="bars bars-middle">
                        <div class="circle circle-3"></div>
                        <div>院校主管单位</div>
                      </div>
                      <div class="bars bars-lang">
                        <div class="circle circle-4"></div>
                        <div>智慧社区</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-5"></div>
                        <div>工厂</div>
                      </div>
                    </div>
                  </div>
                  <div class="kanban-img"></div>
                </div>
              </el-tab-pane>
              <el-tab-pane label="配电设备抢修维修" name="3">
                <div class="rotation-7">
                  <div class="kanban-details">
                    <div class="kb-title">
                      <div class="bold-line"></div>
                      <div>配电室智能监控11</div>
                    </div>
                    <div class="kb-desc">
                      实时全方位监视用户配电系统的运行状态和电量数据，提供
                      用户概括，电力数据监测，电能质量分析，用电分析，日/
                      月/年用能数据报表，异常事件报警和记录，运行，环境监测
                      运维管理等功能
                    </div>
                    <div class="scene">应用场景</div>
                    <div class="explain-bar">
                      <div class="bars bars-lang">
                        <div class="circle circle-1"></div>
                        <div>电力运行维护企业</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-2"></div>
                        <div>集团企业</div>
                      </div>
                      <div class="bars bars-middle">
                        <div class="circle circle-3"></div>
                        <div>院校主管单位</div>
                      </div>
                      <div class="bars bars-lang">
                        <div class="circle circle-4"></div>
                        <div>智慧社区</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-5"></div>
                        <div>工厂</div>
                      </div>
                    </div>
                  </div>
                  <div class="kanban-img"></div>
                </div>
              </el-tab-pane>
              <el-tab-pane label="配电设备升级改造" name="4">
                <div class="rotation-7">
                  <div class="kanban-details">
                    <div class="kb-title">
                      <div class="bold-line"></div>
                      <div>配电室智能监控11</div>
                    </div>
                    <div class="kb-desc">
                      实时全方位监视用户配电系统的运行状态和电量数据，提供
                      用户概括，电力数据监测，电能质量分析，用电分析，日/
                      月/年用能数据报表，异常事件报警和记录，运行，环境监测
                      运维管理等功能
                    </div>
                    <div class="scene">应用场景</div>
                    <div class="explain-bar">
                      <div class="bars bars-lang">
                        <div class="circle circle-1"></div>
                        <div>电力运行维护企业</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-2"></div>
                        <div>集团企业</div>
                      </div>
                      <div class="bars bars-middle">
                        <div class="circle circle-3"></div>
                        <div>院校主管单位</div>
                      </div>
                      <div class="bars bars-lang">
                        <div class="circle circle-4"></div>
                        <div>智慧社区</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-5"></div>
                        <div>工厂</div>
                      </div>
                    </div>
                  </div>
                  <div class="kanban-img"></div>
                </div>
              </el-tab-pane>
              <el-tab-pane label="电能质量提升" name="5">
                <div class="rotation-7">
                  <div class="kanban-details">
                    <div class="kb-title">
                      <div class="bold-line"></div>
                      <div>配电室智能监控11</div>
                    </div>
                    <div class="kb-desc">
                      实时全方位监视用户配电系统的运行状态和电量数据，提供
                      用户概括，电力数据监测，电能质量分析，用电分析，日/
                      月/年用能数据报表，异常事件报警和记录，运行，环境监测
                      运维管理等功能
                    </div>
                    <div class="scene">应用场景</div>
                    <div class="explain-bar">
                      <div class="bars bars-lang">
                        <div class="circle circle-1"></div>
                        <div>电力运行维护企业</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-2"></div>
                        <div>集团企业</div>
                      </div>
                      <div class="bars bars-middle">
                        <div class="circle circle-3"></div>
                        <div>院校主管单位</div>
                      </div>
                      <div class="bars bars-lang">
                        <div class="circle circle-4"></div>
                        <div>智慧社区</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-5"></div>
                        <div>工厂</div>
                      </div>
                    </div>
                  </div>
                  <div class="kanban-img"></div>
                </div>
              </el-tab-pane>
              <el-tab-pane label="电力技术咨询" name="6">
                <div class="rotation-7">
                  <div class="kanban-details">
                    <div class="kb-title">
                      <div class="bold-line"></div>
                      <div>配电室智能监控11</div>
                    </div>
                    <div class="kb-desc">
                      实时全方位监视用户配电系统的运行状态和电量数据，提供
                      用户概括，电力数据监测，电能质量分析，用电分析，日/
                      月/年用能数据报表，异常事件报警和记录，运行，环境监测
                      运维管理等功能
                    </div>
                    <div class="scene">应用场景</div>
                    <div class="explain-bar">
                      <div class="bars bars-lang">
                        <div class="circle circle-1"></div>
                        <div>电力运行维护企业</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-2"></div>
                        <div>集团企业</div>
                      </div>
                      <div class="bars bars-middle">
                        <div class="circle circle-3"></div>
                        <div>院校主管单位</div>
                      </div>
                      <div class="bars bars-lang">
                        <div class="circle circle-4"></div>
                        <div>智慧社区</div>
                      </div>
                      <div class="bars">
                        <div class="circle circle-5"></div>
                        <div>工厂</div>
                      </div>
                    </div>
                  </div>
                  <div class="kanban-img"></div>
                </div>
              </el-tab-pane>
            </el-tabs>
          </div>
        </div>
      </div>
    </div>
    <div class="block-4">
      <div class="view-1">
        <div class="cloud"></div>
        <div class="advantage">
          <div class="adv-content">
            <p class="adv-title">方案优势</p>
            <div class="bottom-line"></div>
            <div class="adv-details">
              全方位一体化解决方案，满足客户的共性要求，提供专业服务，为客户降低成本，提供精准的决策
              依据，全方面提升市场核心竞争力，实现利润最大化。
            </div>
          </div>
        </div>
      </div>
      <div class="view-2">
        <div class="safe-area">
          <div class="two-img">
            <div class="img-1"></div>
            <div class="img-2"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="block-5">
      <div class="safe-area">
        <div class="case">
          <p class="case-title">客户案例</p>
          <div class="bottom-line"></div>
          <el-carousel indicator-position="none" :autoplay="false">
            <el-carousel-item v-for="item in 4" :key="item">
              <div class="case-list">
                <div class="img-font">
                  <div class="img">
                    <div class="introduce">
                      <div class="intr-title">实现功能</div>
                      <div class="intr-details">
                        <div class="intr-list">
                          <div class="one-info">
                            <i class="iconfont icon-ok"></i>
                            <span>全面可靠</span>
                            <span>实时监控/数据采集/预警报警/风险掌控</span>
                          </div>
                          <div class="one-info">
                            <i class="iconfont icon-ok"></i>
                            <span>专业安全</span>
                            <span>快捷应急响应/精良监测设备/专业运维团队</span>
                          </div>
                          <div class="one-info">
                            <i class="iconfont icon-ok"></i>
                            <span>提升效率</span>
                            <span>集中管理/高效工作/数据分析/资产管理</span>
                          </div>
                          <div class="one-info">
                            <i class="iconfont icon-ok"></i>
                            <span>智能增效</span>
                            <span
                              >能耗监控/趋势分析预测/节能降耗增效/优化人员配备</span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="describe">
                    <div class="desc-title">环普科技产业园</div>
                    <div class="desc-details">
                      项目简介:环普，亚洲最大的物流基础设施供应商和服务商-新加坡普洛斯集团新兴成员，致力于现代综合产业园的投资与发展。环普产业园配电室位于负一层，一期设两座（一
                      期主配、一期分配）配电室，二期设两座（二期主配、二期分配）配电室，总设计容量26950KVA。
                    </div>
                  </div>
                </div>
              </div>
            </el-carousel-item>
          </el-carousel>
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
      index: 0,
      imgList: [
        { url: '/img/transtion.png' },
        { url: '/img/transtion-details.png' },
        { url: '/img/transtion.png' },
        { url: '/img/transtion.png' },
      ],
    }
  },
  mounted() {
    $('#footer').css('display', 'block')
    $('#header').css('position', 'fixed')
    $(window).scroll(function () {
      var top = $(document).scrollTop()
      this.scrollTop = top
      if (top >= 590) {
        $('.link-a ').css('color', '#333333')
        $('#header').css('background-color', '#ffffff')
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
  background: url('/img/solution.jpg') no-repeat;
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
        @include bgImg(463px, 418px, '/img/toup.png');
      }
    }
  }
  .block-2 {
    display: flex;
    justify-content: center;
    height: 928px;
    background: #f5f5f5;
    .describe {
      width: 1160px;
      text-align: center;
      color: #202020;
      font-weight: bold;
      .desc-title {
        margin-top: 80px;
        font-size: 40px;
      }
      .bottom-line {
        margin: 0 auto;
        width: 40px;
        height: 5px;
        background: #085e68;
        margin-top: 5px;
      }
      .desc-details {
        margin-top: 38px;
        display: flex;
        align-items: center;
        height: 280px;
        .left-details {
          width: 600px;
          height: 242px;
          background-color: #586985;
          .equipment {
            margin-top: 35px;
            @include bgImg(482px, 189px, '/img/solution_overview.png');
          }
        }
        .right-details {
          width: 544px;
          height: 280px;
          background: #ffffff;
          box-shadow: -20px 0px 10px 3px rgba(12, 16, 27, 0.06);
          border-radius: 10px;
          .summary {
            margin: 40px 29px 61px 34px;
            .sum-title {
              height: 26px;
              padding-left: 10px;
              border-left: 3px solid #085e68;
              text-align: left;
            }
            .sum-details {
              margin-top: 28px;
              p {
                width: 475px;
                font-size: 14px;
                font-family: Microsoft YaHei;
                font-weight: bold;
                color: #999999;
                line-height: 30px;
              }
            }
          }
        }
      }
      .rotation {
        margin-top: 100px;
        width: 1150px;
        height: 260px;
      }
    }
  }
  .block-3 {
    display: flex;
    justify-content: center;
    height: 713px;
    background: url('/img/function.png') no-repeat;
    .function {
      width: 1140px;
      .view-1 {
        font-size: 40px;
        font-family: Microsoft YaHei;
        color: #202020;
        text-align: center;
        margin-top: 50px;
        font-weight: bold;
      }
      .view-2 {
        margin-top: 40px;
         .rotation-7 {
           margin-top: 50px;
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
              color: #999999;
            }
            .scene {
              margin-left: 10px;
              margin-top: 20px;
              font-size: 14px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #454b4c;
            }
            .explain-bar {
              display: flex;
              flex-wrap: wrap;
              margin-left: 10px;
              margin-top: 15px;
              .bars-lang {
                width: 150px !important;
              }
              .bars-middle {
                width: 120px !important;
              }
              .bars {
                width: 100px;
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
                  margin-right: 10px;
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
            width: 661px;
            height: 402px;
            background: url('/img/program-chart.png') no-repeat;
          }
        }
        .line {
          margin-top: 13px;
          height: 1px;
          background: #e2e2e2;
        }
      }

      // 深度穿透ele样式
      .view-2::v-deep {
        .el-tabs__nav-scroll {
          display: flex;
          justify-content: center;
        }
        .el-tabs__nav-wrap::after {
          height: 1px;
          background: #e2e2e2;
        }
        .el-tabs__item {
          padding: 0 29px;
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
      .view-5 {
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
    }
  }
  .block-4 {
    height: 651px;
    background: url('/img/advantage.png') no-repeat;
    .view-1 {
      display: flex;
      .cloud {
        width: 825px;
        height: 649px;
        @include bgImg(825px, 649px, '/img/cloud-room.png', cover);
      }
      .advantage {
        .adv-content {
          margin-top: 100px;
          margin-left: 47px;
          .adv-title {
            font-size: 40px;
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #ffffff;
            margin-left: 5%;
          }
          .bottom-line {
            margin: 0 auto;
            width: 40px;
            height: 5px;
            background: #085e68;
            margin-top: 5px;
            margin-left: 15%;
          }
          .adv-details {
            margin-top: 30px;
            width: 618px;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #ffffff;
          }
        }
      }
    }
    .view-2 {
      height: 200px;
      position: absolute;
      margin-top: -258px;
      width: 100%;
      display: flex;
      justify-content: center;
      .safe-area {
        justify-content: flex-end;
        .two-img {
          width: 1058px;
          @include flex();
          .img-1 {
            @include bgImg(501px, 200px, '/img/service.png');
          }
          .img-2 {
            @include bgImg(501px, 200px, '/img/magnifier.png');
          }
        }
      }
    }
  }
  .block-5 {
    display: flex;
    justify-content: center;
    background: url('/img/case.jpg') no-repeat;
    height: 900px;
    .case::v-deep {
      .el-carousel__container {
        height: 563px;
      }
    }
    .case {
      width: 100%;
      margin-top: 107px;
      .case-title {
        font-size: 40px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #202020;
        text-align: center;
      }
      .bottom-line {
        margin: 0 auto;
        width: 40px;
        height: 5px;
        background: #085e68;
        margin-top: 5px;
      }

      .case-list {
        margin-top: 61px;
        background-color: #ffffff;
        width: 1200px;
        height: 502px;
        box-shadow: -7px 0px 46px 0px rgba(223, 234, 235, 0.49);
        border-radius: 10px;
        .img-font {
          .img {
            width: 1200px;
            height: 346px;
            border-radius: 8px;
            background: url('/img/solution.jpg') no-repeat;
            .introduce {
              width: 497px;
              padding: 136px 0 0 56px;
              .intr-title {
                font-size: 20px;
                font-family: Source Han Sans CN;
                font-weight: bold;
                color: #ffffff;
              }
              .intr-details {
                margin-top: 20px;
                font-size: 14px;
                font-family: Source Han Sans CN;
                font-weight: bold;
                color: #ffffff;
                width: 497px;
                height: 142px;
                background-color: rgba($color: #085e68, $alpha: 0.82);
                border-radius: 10px;
                .intr-list {
                  padding: 20px 0 0 15px;
                  .one-info {
                    margin-bottom: 6px;
                    .icon-ok {
                      color: #ffffff;
                      font-size: 14px;
                    }
                    span {
                      margin-left: 20px;
                    }
                  }
                }
              }
            }
          }
          .describe {
            width: 1150px;
            margin: 40px auto;
            .desc-title {
              font-size: 20px;
              font-family: Source Han Sans CN;
              font-weight: bold;
              color: #202020;
            }
            .desc-details {
              font-size: 14px;
              margin-top: 17px;
              font-family: Source Han Sans CN;
              font-weight: bold;
              color: #999999;
            }
          }
        }
      }
    }
  }
}
</style>
