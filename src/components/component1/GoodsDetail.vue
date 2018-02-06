<template>
    <div class="goods">
       <!-- header -->
        <div class="goods_top" @click="back"></div>
        <!-- title -->
        <div class="goods_List">
            <ul class="goods_content">
                <li class="content">
                    <h1><img :src="tempGoods.avatar" alt=""></h1>
                    <span class="brand">品牌</span>
                    <span class="sell">{{ tempGoods.name }}</span>
                    <span class="note">></span>
                </li>
                <li class="numbers">
                    <span class="start">{{ tempGoods.rating }}</span>
                    <span class="mar">{{tempGoods.recent_order_num}}</span>
                    <span class="time">{{ tempGoods.time }}</span>
                    <span class="range">{{ tempGoods.range}}</span>
                </li>
            </ul>
            <p>欢迎光临,用餐高峰期请提前下单，谢谢。</p>
        </div>
        <!-- 首单 -->
        <div class="favour_news">
            <ul class="first_mune clearfix">
              <li class="shou fl">首单</li>
              <li class="new_user fl">新用户下单，立减17元(不与其他活动同享)</li>
              <li class="favour fl" @click="showShadow">3个优惠</li>
            </ul>
        </div>
        <!-- 遮罩层 -->
        <div class="shadow" v-show="isShow">
            <div class="detail-wrapper clearfix">
                <div class="derail-main">
                    <li class="content">
                        <span class="brand">品牌</span>
                        <span class="sell">{{ tempGoods.name }}</span>
                        <span class="note">></span>
                    </li>
                </div>
            </div>
            <div class="detali-close">
                <span></span>
            </div>
        </div>
       
            
       
    </div>
</template>
  
<script>
export default {
    name: "GoodsDetail",
    data () {
        return {
          // recommend:[],
          tempGoods: {
            name: '',
            avatar: ''
          },
          isShow:false
        };
    },
    methods:{
        back(){
          this.$router.go(-1)
        },
        showShadow(){
          this.isShow = true
        }
    },
    created(){
      this.$http.get('/api/recommend')
      .then((res) => {
          this.recommend = res.data.data
          for(var tempGoods of res.data.data){
            if(this.$route.params.goodsId == tempGoods.id){
              this.tempGoods = tempGoods
            }
          }
      })
    },
}
</script>
  
<style lang="css" scoped>
    /* header */
    li{
      list-style: none;
    }
  .goods .goods_top{
    width: 100%;
    height: 0.68rem;
    background:url(./img/images/good_03.gif) #424443 no-repeat 0.2rem 0.1rem;
  }
  .goods_content{
    padding:0 0.2rem;
    text-align: center;
    font-size: 0.12rem;
    margin-top: 0.1rem;
  }
  .goods_content .content img{
    width: 0.75rem;
  }
  .goods_content .content .brand{
    display: inline-block;
    width: 0.4rem;
    height: 0.15rem;
    background: #ffe924;
    margin-right: 0.2rem;
  }
  .goods_content .sell{
    font-size: 0.2rem;
    font-weight: bold;
    margin-right: 0.15rem;
  }
  .goods_content .numbers{
    margin:0.1rem 0 0.1rem 0;
  }
  .numbers span{
    padding: 0 0.07rem;
  }
  .goods_List p{
    width: 2.2rem;
    font-size: 0.1rem;
    color:#b0b0b0;
    margin: 0 auto;
  }
  /* 首单 */
  .first_mune{
    margin-left: 0.4rem;
    margin-top: 0.1rem;
    color:#666;
  }
  .first_mune .shou{
    width: 0.3rem;
    height: 0.15rem;
    background: #70bc46;
    color: #fff;
    margin-right: 0.1rem;
  }
  .first_mune .favour{
    width: 0.5rem;
    height: 0.2rem;
    margin-left: 0.07rem;
  }
  .shadow{
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 100;
    overflow: auto;
    background: rgba(7, 17, 27, 0.5);
  }
 
 

</style>