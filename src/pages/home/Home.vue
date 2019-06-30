<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <HomeIcons :list="iconList"></HomeIcons>
    <home-recommend :list="recommendList"></home-recommend>
  </div>
</template>

<script>
import HomeHeader from './compoments/Header'
import HomeSwiper from './compoments/Swiper'
import HomeIcons from './compoments/Icons'
import HomeRecommend from './compoments/Recommend'
import axios from 'axios'

export default {
  name: 'Home',
  components: {
    HomeIcons,
    HomeSwiper,
    HomeHeader,
    HomeRecommend
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconList: [],
      recommendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style scoped>

</style>
