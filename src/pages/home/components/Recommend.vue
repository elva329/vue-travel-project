<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom"
      v-for="item of recommendList"
      :key = "item.id"
      >
          <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/b1fec098-eae6-426f-a3fc-a9ccdc9d3730.jpg_r_480x320x90_3b53e5e0.jpg',
          title: '南昌-三亚 5天自由行',
          desc: '嗨爆亲子酒店☪3.3万㎡水乐园✪三亚湾红树林☛游艇出海含潜水+旅拍+房型升级">嗨爆亲子酒店☪3.3万㎡水乐园✪三亚湾红树林☛游艇出海含潜水+旅拍+房型升级'
        },
        {
          id: '0002',
          imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/ff46c586-e758-4d7b-b1fe-fa36a4712233.jpg_r_480x320x90_a1bf4301.jpg',
          title: '南昌-凤凰古城 4天跟团游',
          desc: '【家庭游】五星纯玩｜一价全含｜张家界天门山大峡谷玻璃桥凤凰4日｜赠魅力湘西秀'
        },
        {
          id: '0003',
          imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/d5e82d7f-cdcd-4626-83e0-c1527ef59736.jpg_r_480x320x90_17f0ede1.jpg',
          title: '南昌-厦门 5天跟团游',
          desc: '网红新选🔥厦门鼓浪屿土楼动车5日-4星酒店连住-厦大赠帆船出海🦀️海鲜餐'
        },
        {
          id: '0004',
          imgUrl: '//imgs.qunarzz.com/p/tts2/1811/50/6eceeef1f4343702.jpg_r_390x260x90_b99fab2d.jpg',
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
  .item
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
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
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
