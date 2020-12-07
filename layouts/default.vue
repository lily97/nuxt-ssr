
<template>
  <div class="container">
    <Header />
    <div class="body">
      <nuxt />
    </div>
    <Footer />
  </div>
</template>
<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'

export default {
  components: {
    Header,
    Footer,
  },
}
</script>

<style lang="scss">
@import '~@/assets/style/mixin.scss';
* {
  margin: 0;
  padding: 0;
}

.box {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.container {
  height: 100vh;
  min-width: 1200px;
  .body {
    z-index: 2;
  }
}
</style>
