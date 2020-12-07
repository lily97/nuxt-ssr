
<template>
  <div class="header" id="header">
    <header class="top-bar">
      <nav class="nav">
        <div class="logo">
          <a href="/">
            <img id="logo" src="/img/logo.png" />
          </a>
        </div>
        <div class="links">
          <nuxt-link
            class="link-a"
            v-for="item in nav"
            :to="item.path"
            :key="item.name"
            exact
            >{{ item.name }}</nuxt-link
          >
        </div>
        <div class="login" @click="platform">平台登录</div>
      </nav>
    </header>
  </div>
</template>
<script>
export default {
  data() {
    return {}
  },
  computed: {
    nav: () => [
      {
        name: '首页',
        path: '/',
      },
      {
        name: '产品与服务',
        path: '/productService',
      },
      {
        name: '解决方案',
        path: '/plan',
      },
      {
        name: '战略合作',
        path: '/cooperation',
      },
      {
        name: '关于我们',
        path: '/about',
      },
    ],
  },

  methods: {
    platform() {
      window.location.href = 'http://platform.guoyuancloud.com/'
    },
  },
  mounted() {},
}
</script>

<style  lang="scss">
@import '~@/assets/style/mixin.scss';
.header {
  z-index: 9999;
  width: 100%;
  height: 80px;
  position: absolute;
  .top-bar {
    width: 1200px;
    @include flex(center);
    margin: 25px auto 0 auto;
    .link_active {
      color: #085e68 !important;
    }
    .nav {
      @include flex();
      width: 1140px;
      .logo {
        width: 119px;
        height: 35px;
      }
      .links {
        margin-left: 380px;
        width: 500px;
        @include flex();
        a {
          text-decoration: none;
        }
      }
      .login {
        width: 90px;
        height: 30px;
        background: #ffffff;
        border-radius: 15px;
        color: #085e68;
        font-weight: bold;
        text-align: center;
        line-height: 30px;
        cursor: pointer;
      }
      .link-a {
        font-size: 14px;
        font-weight: bold;
        color: #ffffff;
        display: block;
      }
    }
  }
}
</style>