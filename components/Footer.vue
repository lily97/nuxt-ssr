
<template>
  <div class="footer" ref="footer" id="footer">
    <div class="Copywriting">
      <div class="describe">
        领先的大数据监控技术，成熟的智慧电力能效管理解决方案
      </div>
      <div class="consulting">立即咨询</div>
    </div>
    <pointwave :color="0x27b7c7" class="wave" />
    <div class="record">豫ICP备2020029860号</div>
  </div>
</template>
<script>
import Pointwave from '@/components/Pointwave'

export default {
  components: {
    Pointwave,
  },
  computed: {
    friends: () => [
      {
        name: '中关村在线',
        url: 'http://www.zol.com.cn/',
      },
      {
        name: 'Z商城',
        url: 'http://www.zol.com/',
      },
    ],
  },
}
</script>
<style lang="scss">
.footer {
  z-index: 1;
  height: 389px;
  position: relative;
  display: none;
  .Copywriting {
    text-align: center;
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-top: 60px;
    .describe {
      font-size: 24px;
      font-weight: bold;
      color: #ffffff;
    }
    .consulting {
      width: 160px;
      height: 43px;
      background: #f5f5f5;
      border-radius: 22px;
      margin-top: 45px;
      font-size: 16px;
      font-weight: bold;
      color: #085e68;
      line-height: 43px;
      cursor: pointer;
    }
  }
  .wave {
    height: 300px;
  }
  .record {
    height: 89px;
    font-size: 14px;
    font-weight: bold;
    color: #74797d;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>