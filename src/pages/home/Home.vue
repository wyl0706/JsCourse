<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <HomeIcons></HomeIcons>
    <home-recommend></home-recommend>
  </div>
</template>

<script>
import HomeHeader from './compoments/Header'
import HomeSwiper from './compoments/Swiper'
import HomeIcons from './compoments/Icons'
import HomeRecommend from './compoments/Recommend'
export default {
  name: 'Home',
  components: {
    HomeIcons,
    HomeSwiper,
    HomeHeader,
    HomeRecommend
  }
}
</script>

<style scoped>

</style>
