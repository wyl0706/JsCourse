<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <HomeIcons></HomeIcons>
  </div>
</template>

<script>
import HomeHeader from './compoments/Header'
import HomeSwiper from './compoments/Swiper'
import HomeIcons from './compoments/Icons'
export default {
  name: 'Home',
  components: {
    HomeIcons,
    HomeSwiper,
    HomeHeader
  }
}
</script>

<style scoped>

</style>
