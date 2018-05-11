<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for='item in page' :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" alt="">
          </div>
          <div class="icon-desc ellipse">{{item.desc}}</div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name:"HomeIcons",
  data(){
    return {
      iconList: [ 
        { id: '0001', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png", desc:'景点门票景点门票景点门票景点门票景点门票'},
        { id: '0002', imgUrl:"http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png", desc:'一日游'},
        { id: '0003', imgUrl:"http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png", desc:'必游榜单'},
        { id: '0004', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png", desc:'动植物园'},
        { id: '0005', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png", desc:'踏青赏花'},
        { id: '0006', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png", desc:'城市观光'},
        { id: '0007', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png", desc:'上海欢乐谷'},
        { id: '0008', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png", desc:'哈哈哈'},
        { id: '0009', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png", desc:'自如方法'},
        { id: '0010', imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png", desc:'海洋世界'},
      ]
    }
  },
  computed:{
    pages(){
      const pages = [];
      this.iconList.forEach((v,i)=>{
        const page = Math.floor(i /8)
        if(!pages[page]){
          pages[page] =[]
        }
        pages[page].push(v)
      })
      return pages
    }
  }
}
</script>

<style lang='scss' scoped>
 @import '~styles/base.scss';
  .icons >>> .swiper-container {
      height: 0;
      padding-bottom: 50%;
  }
  .icons{
    .icon{
      position: relative;
      float: left;
      width:25%;
      height: 0;
      padding-bottom: 25%;
      overflow: hidden;
      .icon-img{
        position: absolute;
        top:0;
        left: 0;
        right: 0;
        box-sizing: border-box;
        bottom: 1.1rem;
        .icon-img-content{
          display: block;
          margin: 0 auto;
          height: 100%;
        }
      }
      .icon-desc{
        width:100%;
        position: absolute;
        height: 1.1rem;
        line-height: 1.1rem;
        bottom: .2rem;
        text-align: center;  
        font-size: 14px;
      }
    }
  }
</style>