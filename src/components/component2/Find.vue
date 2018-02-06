<template>
    <div class="find">
        <div class='top'>
            <h1>发现</h1>
        </div>
        <div class='top_center'>
           <ul class='oneUl'>
                <li v-for='item in find' :key='item.id'><a href="#"><div class='zongdiv'><p>{{ item.title }}</p><p>{{ item.subtitle }}</p></div><img :src="item.url"></a></li> 
                <!-- <li><a href="#"><div class='onediv zongdiv'><p>金币商城</p><p>0元好物在这里</p></div><img src="https://fuss10.elemecdn.com/8/38/9c9aea0e856149083d84af3444b78jpeg.jpeg?imageMogr/format/webp/"></a></li> 
                <li><a href="#"><div class='twodiv zongdiv'><p>有红包快抢</p><p>礼包福利不停</p></div><img src="https://fuss10.elemecdn.com/f/85/2bb180f2052c33cfec3852ef2bfccjpeg.jpeg?imageMogr/format/webp/"></a></li>
                <li><a href="#"><div class='threediv zongdiv'><p>必吃爆料</p><p>最好外卖指南</p></div><img src="https://fuss10.elemecdn.com/2/36/b784087aff96a97f4e5183d0d784fjpeg.jpeg?imageMogr/format/webp/"></a></li>
                <li><a href="#"><div class='fourdiv zongdiv'><p>推荐有奖</p><p>5元现金不停</p></div><img src="https://fuss10.elemecdn.com/6/76/8d42eef97ff4c1c2b671085358541jpeg.jpeg?imageMogr/format/webp/"></a></li>
                <li><a href="#"><div class='fivediv zongdiv'><p>周边优惠</p><p>领取口碑好券</p></div><img src="https://fuss10.elemecdn.com/5/10/2351e989d4171479ba0d7b5c06053jpeg.jpeg?imageMogr/format/webp/"></a></li>
                <li><a href="#"><div class='sixdiv zongdiv'><p>百元红包</p><p>兴业银行联名卡</p></div><img src="https://fuss10.elemecdn.com/3/cc/a45d2b9d7d09bbc49b40d4e626093jpeg.jpeg?imageMogr/format/webp/"></a></li> -->
           </ul>
           <div class='bander'>
               <a href="#"><img src="https://fuss10.elemecdn.com/b/6d/656006edcd86033a1b32b23ddea37jpeg.jpeg?imageMogr/format/webp/"></a>
           </div>
        </div>
        <div class='center'>
            <div class='center_top'>
                <div class='center_topdiv'>
                    <img src="./img/下载_03.jpg">
                    <span>为你推荐</span>
                 </div>
                 <h4>你的口味我都懂得</h4>
            </div>
            <div class="center_center">
                <ul class='twoUl'>
                    <li class='zongli' v-for='item in foods' :key='item.id'>
                        <a href="#">
                            <img :src="item.food.url">
                            <p class='onep'>{{ item.food.name }}</p>
                            <p class='twop'>月售{{ item.food.month_sales }}份<span>{{ item.food.food_rate }}</span></p>
                            <p class='threep'>￥{{ item.food.price }}<span>{{ item.food.descriptions }}</span></p>
                            <p class='fourp'>{{ item.restaurant.name }}</p>
                        </a>
                    </li>
                    <!-- <li class='li2 zongli'>
                        <a href="#">
                            <img src="https://fuss10.elemecdn.com/3/48/486f9cdd9c57840341d4109232944jpeg.jpeg?imageMogr/format/webp/thumbnail/!345x345r/gravity/Center/crop/345x345">
                            <p class='onep'>酸菜排骨米饭套餐</p>
                            <p class='twop'>月售756份<span>好评率99%</span></p>
                            <p class='threep'>￥29.9<span>满20减18</span></p>
                            <p class='fourp'>小火慢炖排骨米饭</p>
                        </a>
                    </li>
                    <li class='li3 zongli'>
                        <a href="#">
                            <img src="https://fuss10.elemecdn.com/7/45/3cad1f1b07ee9527b4aa2c268023cjpeg.jpeg?imageMogr/format/webp/thumbnail/!345x345r/gravity/Center/crop/345x345/">
                            <p class='onep'>酸菜排骨米饭套餐</p>
                            <p class='twop'>月售756份<span>好评率99%</span></p>
                            <p class='threep'>￥29.9<span>满20减18</span></p>
                            <p class='fourp'>小火慢炖排骨米饭</p>
                        </a>
                    </li>
                    <li class='li4 zongli'>
                        <a href="#">
                            <img src="https://fuss10.elemecdn.com/7/45/3cad1f1b07ee9527b4aa2c268023cjpeg.jpeg?imageMogr/format/webp/thumbnail/!345x345r/gravity/Center/crop/345x345/">
                            <p class='onep'>酸菜排骨米饭套餐</p>
                            <p class='twop'>月售756份<span>好评率99%</span></p>
                            <p class='threep'>￥29.9<span>满20减18</span></p>
                            <p class='fourp'>小火慢炖排骨米饭</p>
                        </a>
                    </li>
                    <li class='li5 zongli'>
                        <a href="#">
                            <img src="https://fuss10.elemecdn.com/0/4a/b824d1e4bac879449a53c739dc582jpeg.jpeg?imageMogr/format/webp/thumbnail/!345x345r/gravity/Center/crop/345x345/">
                            <p class='onep'>酸菜排骨米饭套餐</p>
                            <p class='twop'>月售756份<span>好评率99%</span></p>
                            <p class='threep'>￥29.9<span>满20减18</span></p>
                            <p class='fourp'>小火慢炖排骨米饭</p>
                        </a>
                    </li>
                    <li class='li6 zongli'>
                        <a href="#">
                            <img src="https://fuss10.elemecdn.com/6/fb/ce95a7e88f382e081b42bf02c6710jpeg.jpeg?imageMogr/format/webp/thumbnail/!345x345r/gravity/Center/crop/345x345/">
                            <p class='onep'>酸菜排骨米饭套餐</p>
                            <p class='twop'>月售756份<span>好评率99%</span></p>
                            <p class='threep'>￥29.9<span>满20减18</span></p>
                            <p class='fourp'>小火慢炖排骨米饭</p>
                        </a>
                    </li> -->
                </ul>
                <div class='huoqu'>
                    <a>获取更多</a>
                </div>
            </div>
            <div class='center_bottom'>
               <div class="bottom1">
                   <div class='bottom1_top'>
                        <a herf='#'>
                            <img src="./img/下载_04.jpg">
                            <span>限时好礼</span>
                            <p>金币换好礼</p>
                        </a>
                   </div>
                   <div class='bottom1_center'>
                       <div class='jingpin'>
                           <a herf='#'>
                                <img src="https://fuss10.elemecdn.com/7/c5/f595b52bc6b50c9899398dccffd42jpeg.jpeg?imageMogr/format/webp/">
                                <p>饿了么7元红包</p>
                                <p>210金币</p>
                           </a>    
                       </div>
                       <div class='jingpin'>
                           <a herf='#'>
                                <img src="https://fuss10.elemecdn.com/d/56/8b479231309654bfa07f28999768bjpeg.jpeg?imageMogr/format/webp/">
                                <p>阳澄湖大闸蟹</p>
                                <p>9金币</p>
                            </a>    
                       </div>
                       <div class='jingpin'>
                           <a herf='#'>
                                <img src="https://fuss10.elemecdn.com/5/78/5c1ca7ceca079926933ca418c9eb7jpeg.jpeg?imageMogr/format/webp/">
                                <p>智能扫地机器人</p>
                                <p>9金币</p>
                            </a>
                       </div>
                   </div>
                   <div class='bottom1_bottom'>
                       <h3>查看更多</h3>
                   </div>
               </div>
               <div class="bottom2">
                   <div class='bottom2_top'>
                       <a herf='#'>
                            <img src="./img/下载_05.jpg">
                            <span>每日精选</span>
                            <p>领券优惠 全场包邮</p>
                       </a>
                   </div>
                   <div class='bottom2_center'>
                        <div class='jingpin1'>
                           <a herf='#'>
                                <img src="https://fuss10.elemecdn.com/0/f4/2b6932859186d9bb6be77854e4821png.png?imageMogr/format/webp/">
                                <p>6瓶西班牙葡萄酒</p>
                                <p>￥79.9</p>
                            </a>
                       </div>
                       <div class='jingpin1'>
                           <a herf='#'>
                                <img src="https://fuss10.elemecdn.com/e/f5/c3e3dbd89973d76f998fc21064c4epng.png?imageMogr/format/webp/">
                                <p>罗莱羽绒被</p>
                                <p>￥75</p>
                           </a>    
                       </div>
                       <div class='jingpin1'>
                           <a herf='#'> 
                                <img src="https://fuss10.elemecdn.com/f/8b/231f91e8304f22397dcaa9b67b71dpng.png?imageMogr/format/webp/">
                                <p>VR虚拟限时眼镜</p>
                                <p>￥29.9</p>
                           </a>
                       </div>
                   </div>
                   <div class='bottom3'>
                       <h3>查看更多</h3>
                   </div>
               </div>
            </div>
            <div class='duoyu'></div>
        </div>
    </div>
</template>
<script>
export default {
    name: "find",
    data () {
        return {
            find: [],
            foods:[]
        };
    },
    created(){
        this.$http.get('/api/find')
        .then((res)=>{
            this.find = res.data.data[0].one
        })
        this.$http.get('/api/foods')
        .then((res) => {
            this.foods = res.data.data[0].items
        })
     },
     methods:{
       
     }
}
</script>
<style lang="css" scoped>
    .top{
        width: 100%;
        height: 0.44rem;
        background: #00a2ff;
        color:#fff;
        font-size: 0.16rem;
        text-align: center;
    }
    .top_center{
        width: 100%;
        height:3.55rem;
    }
    .oneUl li{
        width: 50%;
        height: 0.8rem;
        border: 0.01rem solid #f5f5f5;
        float: left;
    }
    .oneUl li a div{
        float: left;
    }
    .oneUl li a img{
        float:left;
        width: 0.45rem;
        height: 0.45rem;
        margin-top:0.24rem;
    }
    .zongdiv{
        width: 1.25rem;
        height:100%;
        padding:0.24rem 0 0 0.15rem;
    }
    .zongdiv p:first-child{
        font-size:0.16rem; 
    }
    .zongdiv p:last-child{
        font-size: 0.12rem;
        color:#999999;
    }
    .oneUl li:nth-of-type(1) div p:first-child{
        color: #ff994f;
    }
    .oneUl li:nth-of-type(2) div p:first-child{
        color:#cc3300 ;
    }
    .oneUl li:nth-of-type(3) div p:first-child{
        color: #f5785d;
    }
    .oneUl li:nth-of-type(4) div p:first-child{
        color: #1ba9e1 ;
    }
    .oneUl li:nth-of-type(5) div p:first-child{
        color: #f5785d ;
    }
    .oneUl li:nth-of-type(6) div p:first-child{
        color: #ff994f ;
    }
    .bander{
        clear: both;
        width: 100%;
        height: 1.14rem;
        background: #f5f5f5;
        padding: 0.13rem 0 0 0;
    }
    .bander a{
        height: 09rem;
    }
    .bander img{
        width: 100%;
        height: 0.9rem;
    }
    .center{
        width: 100%;
        height: 9.5rem;
    }
    .center_top{
        width: 100%;
        height: 0.67rem;
        padding: 0.22rem 0 0 1.38rem;
    }
    .center_topdiv{
        width:1.3rem ;
        height: 0.2rem;
    }
    .center_topdiv img{
        width: 0.19rem;
        height: 0.19rem;
        float: left;
    }
   .center_topdiv span{
       font-size: 0.16rem;
       float: left;
       margin-left:0.08rem;
   }
   .center_top h4{
       clear: both;
       width:1.1rem;
       font-size: 0.12rem;
       color:#999999;
   }
   .center_center{
       height: 8.67rem;
   }
   .zongli{
       width:1.72rem;
       height: 2.65rem;
       float: left; 
       margin-left: 0.09rem;
       border: 0.01rem solid red;
   }
   .zongli a p{
       margin:0.03rem 0 0 0.1rem;
   }
   .zongli a img{
       width:100%; 
       height: 1.72rem;
   }
   .twoUl li:nth-of-type(3){
        margin: 0.1rem 0 0.1rem 0.09rem;
   }
   .twoUl li:nth-of-type(4){
        margin: 0.1rem 0 0.1rem 0.09rem;
   }
   .onep{
       font-size:0.16rem;
       color:#444444;
   }
   .twop{
       font-size:0.12rem;
       color:#7d7d7d;
   }
   .twop span{
       margin-left: 0.1rem;
   }
   .threep{
       font-size:0.14rem;
       color:red;
       margin-top:0.01rem;
   }
   .threep span{
       font-size: 0.12rem;
       color:rgb(175, 33, 33);
       border: 0.01rem solid rgb(175, 33, 33);
       margin-left: 0.05rem;
   }
   .fourp{
       font-size:0.12rem;
       color:#acacac;
       margin-top: 0.2rem;
   }
   .huoqu{
       clear: both;
       width: 100%;
       height: 0.5rem;
       font-size: 0.16rem;
       line-height:0.5rem; 
       text-align: center;
       padding-top: 0.15rem;
   }
   .center_bottom{
       margin-top:0.3rem;
       width: 100%;
   }
   .bottom1{
       height: 2.97rem;
   }
   .bottom1_top{
       height: 0.65rem;
       font-size: 0.16rem;
       text-align: center;
       padding-top: 0.15rem;
   }
   .bottom1_top a p{
       clear: both;
       font-size: 0.12rem;
       color:#e2e2e2;
   }
   .bottom1_top img{
       display: inline-block;
   }
   .bottom1_center{
       height: 1.9rem;
   }
   .bottom1_center div:nth-of-type(2){
       margin: 0 0.09rem 0 0.10rem;
   }
   .bottom1_center div:nth-of-type(1){
       margin-left:0.05rem; 
   }
   .jingpin{
       width: 1.15rem;
       height: 1.6rem;
       float:left;
       font-size: 0.14rem;
   }
   .jingpin img{
       width: 100%;
       height: 1rem;
   }
   .jingpin a p{
       padding-left:0.1rem;
   }
   .jingpin  a p:first-child{
        color:#7c7c7c;
        margin-top: 0.35rem;
    }
   .jingpin a p:last-child{
       color:#ff9180;
       margin-top: 0.15rem;
   }
   .bottom1_bottom{
       height: 0.45rem;
       text-align: center;
   }
   .bottom1_bottom h3{
       font-size: 0.18rem;
       color:#ababab;
   }
   .bottom2{
       clear: both;
       height: 3rem;
       margin-top: 0.12rem;
   }
   .bottom2_top{
       height: 0.65rem;
       font-size: 0.16rem;
       text-align: center;
       padding-top: 0.15rem;
   }
   .bottom2_top a p{
       clear: both;
       font-size: 0.12rem;
       color:#e2e2e2;
   }
   .bottom2_top img{
       display: inline-block;
   }
   .bottom2_center{
       height: 1.9rem;
   }
   .bottom2_center div:nth-of-type(2){
       margin: 0 0.09rem 0 0.10rem;
   }
   .bottom2_center div:nth-of-type(1){
       margin-left:0.05rem; 
   }
   .jingpin1{
       width: 1.15rem;
       height: 1.6rem;
       float:left;
       font-size: 0.14rem;
   }
   .jingpin1 img{
       width: 100%;
       height: 1rem;
   }
   .jingpin1 a p{
       padding-left: 0.1rem;
   }
   .jingpin1 a p:first-child{
        color:#7c7c7c;
        margin-top: 0.35rem;
    }
   .jingpin1 a p:last-child{
       color:#ff9180;
       margin-top: 0.15rem;
   }
   .bottom3{
       width: 100%;
       height: 0.45rem;
       text-align: center;
   }
   .bottom3 h3{
       font-size: 0.18rem;
       color:#ababab;
   }
   .duoyu{
        width: 100%;
        height: 0.5rem;
        background:#f5f5f5; 
    }
</style>
