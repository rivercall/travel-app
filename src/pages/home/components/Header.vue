<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont">&#xe624;</div>
    </div>
    <div class="header-input ellipse" >
      <span class="iconfont ">&#xe632;</span>
      请输入城市/景点/游玩名称
    </div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang='scss'>
  @import '~styles/base.scss';

  .header {
    display: flex;
    font-size:14px;
    line-height: 2.1rem;
    color:#fff;
    background:$bgcolor;
    .header-left{
      width:1.61rem;
      div{
        text-align: center;
        font-size:1rem
      }
    }
    .header-input{
      flex:1;
      padding-left: .5rem;
      margin-top: .3rem;
      margin-left:.5rem;
      border-radius:.2rem;
      background:#fff;
      color:#ccc;
      height: 1.5rem;
      line-height: 1.5rem;
    }
    .header-right{
      margin: 0 .5rem;
      text-align: center;
      .iconfont{
        font-size: .5rem
      }
    }
  }
    
</style>