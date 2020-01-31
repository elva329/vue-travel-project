<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom"
      v-for="item of recommendList"
      :key = "item.id"
      >
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl"/>
      </div>  
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/b1fec098-eae6-426f-a3fc-a9ccdc9d3730.jpg_r_480x320x90_3b53e5e0.jpg',
          title: '南昌-三亚 5天自由行',
          desc: '//imgs.qunarzz.com/p/p70/1809/e7/4941057a6aae702.jpg_256x160_9fee6ccb.jpg'
        },
        {
          id: '0002',
          imgUrl: '//imgs.qunarzz.com/p/p66/201304/17/384810d022dd28f793835fbb.jpg_256x160_6a7ec251.jpg',
          title: '南昌-凤凰古城 4天跟团游',
          desc: '【家庭游】五星纯玩｜一价全含｜张家界天门山大峡谷玻璃桥凤凰4日｜赠魅力湘西秀'
        },
        {
          id: '0003',
          imgUrl: '//imgs.qunarzz.com/p/p27/201302/28/d14185ac8a47f6f993835fbb.jpg_256x160_c2ab9336.jpg',
          title: '南昌-厦门 5天跟团游',
          desc: '网红新选🔥厦门鼓浪屿土楼动车5日-4星酒店连住-厦大赠帆船出海🦀️海鲜餐'
        },
        {
          id: '0004',
          imgUrl: '//imgs.qunarzz.com/p/p29/201302/28/3d20251a1b60350a93835fbb.jpg_256x160_e8f468b0.jpg',
          title: '南昌-香港 5天跟团游',
          desc: '春节特惠♕双飞港澳5天❖港珠澳大桥丨海洋公园☛夜游维港☛接机☛赠送迪士尼乐园'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    height: 0
    overflow: hidden
    padding-bottom: 62.5%
  .item-img
      width: 100%
  .item-info
      padding: .1rem
      min-width: 0
    .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
    .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
</style>
