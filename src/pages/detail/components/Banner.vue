<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="https://imgs.qunarzz.com/p/tts9/1706/30/219d20ea05310902.jpg_r_390x260x90_0f069e53.jpg" />
      <div class="banner-info">
        <div class="banner-title">亲子广州珠海双长隆☀2晚熊猫+2晚企鹅☀企鹅自助餐+动物园+马戏+海洋王国</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe609;</span>
        </div>
      </div>
    </div>
    <common-gallery
      :imgs="imgs"
      v-show="showGallery"
      @close="handleGalleryClose"
    >
    </common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false,
      imgs: ['https://imgs.qunarzz.com/p/tts9/1706/30/219d20ea05310902.jpg_r_390x260x90_0f069e53.jpg','https://imgs.qunarzz.com/p/tts9/1706/30/219d20ea05310902.jpg_r_390x260x90_0f069e53.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  },
  components: {
    CommonGallery
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position:relative
    overflow: hidden
    height: 0
    padding-bottom: 66.67%
    .banner-img
      width:100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      backgroun-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
