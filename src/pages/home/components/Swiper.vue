<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-image" :src="item.imgUrl" />>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
  <!-- padding-bottom: height/width -->
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1580398986704&di=6378038134fa8f5aaddf8fbe0b9f3bfd&imgtype=0&src=http%3A%2F%2Fimg2.3lian.com%2F2014%2Ff2%2F66%2Fd%2F98.jpg'
        },
        {
          id: '0002',
          imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1580398998544&di=5d336ff5f8ca4cb382e499465d399629&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201210%2F04%2F20121004214233_Syfid.jpeg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
 .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
 .wrapper
    overflow:hidden
    width:100%
    height:0
    padding-bottom:62.5%
    background:#eee
    .swiper-image
      width:100%
</style>
