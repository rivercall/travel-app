<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.url" >
      </swiper-slide>
      
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    data(){
      return {
        swiperOption: {
          pagination:'.swiper-pagination',
          loop:true
        },
        swiperList:[
          {
            id:'0001',
            url:'http://img1.qunarzz.com/piao/fusion/1804/15/9250dbc86a456302.jpg_750x200_b423f532.jpg'
          },
          {
            id:'0002',
            url:'http://img1.qunarzz.com/piao/fusion/1804/d1/2ba49f4f21ed2102.jpg_750x200_79e641ad.jpg'
          }
        ]
      }
    }
  }
</script>

<style  lang='scss' scoped>
// 样式穿透有些问题
  .wrapper  >>> .swiper-pagination-bullet-active{
    background:#fff !important;
    text-align: center
  }
  .wrapper{
    width: 100%;
    height: 0;
    padding-bottom:26.67%;
    overflow: hidden;
  }
  .swiper-img{
    width: 100%
  }
  
</style>