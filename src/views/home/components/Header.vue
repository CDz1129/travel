<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe658;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe63c;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe65c;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  },
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  display: flex
  line-height: $headerHeight
  background: $bgColor
  color: #fff
  .header-left
    width: 0.64rem
    float: left
    .back-icon
      text-align: center
      font-size: 0.4rem
  .header-input
    flex: 1
    height: 0.64rem
    line-height: 0.64rem
    margin-top: 0.12rem
    background: #fff
    border-radius: 0.1rem
    padding-left: 0.2rem
    color: #ccc
  .header-right
    min-width: 1.04rem
    padding: 0 0.1rem
    float: right
    text-align: center
    color: #fff
    .arrow-icon
      margin-left: -0.04rem
      font-size: 0.3rem
</style>
