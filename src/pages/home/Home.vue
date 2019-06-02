<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
  </div>
</template>

<script>
import HomeHeader from './compoments/Header'
import HomeSwiper from './compoments/Swiper'
export default {
  name: 'Home',
  components: {
    HomeSwiper,
    HomeHeader
  }
}
</script>

<style scoped>

</style>
