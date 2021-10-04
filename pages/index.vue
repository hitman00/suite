<template>
  <div :class="$style.main">
    <Header />
    <Numbers />
    <Slide />
    <GetReady />
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header/Header.vue'
import Numbers from '@/components/Numbers/Numbers.vue'
import Slide from '@/components/Slide/Slide.vue'
import GetReady from '@/components/GetReady/GetReady.vue'
import Footer from '@/components/Footer/Footer.vue'
export default {
  components: {
    Header,
    Numbers,
    Slide,
    GetReady,
    Footer,
  },
}
</script>

<style lang="scss" module>
.main {
  overflow: hidden;
  position: relative;
}
</style>
