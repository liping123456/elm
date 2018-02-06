<template>
    <div class="home">
        <!-- 头部 -->
<<<<<<< HEAD
<<<<<<< HEAD
        <div class="header">
            <p class="address">上地信息产业基地</p>
            <div class="search">
                <input type="search" placeholder="搜索商家、商品名称">
            </div>
            <img src="https://fuss10.elemecdn.com/0/cf/e16c1687a4ea84674d5b531623934png.png?imageMogr/format/webp/thumbnail/!750x210r/gravity/Center/crop/750x210/" alt="">
        </div>
        
=======
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
        <div class="header clearfix">
            <p class="address">上地信息产业基地</p>
            <form>
                <input type="search" placeholder="搜索商家、商品名称">
            </form>
            <div class="images">
                <img src="https://fuss10.elemecdn.com/0/cf/e16c1687a4ea84674d5b531623934png.png?imageMogr/format/webp/thumbnail/!750x210r/gravity/Center/crop/750x210/" alt="">
            </div>
        </div>
<<<<<<< HEAD
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
        <!--分类  -->
        <ul class="kind clearfix">
            <li class="fl" v-for="product of delicious" :key="product.id">
                <a href="javascript:">
                    <img :src="product.img">
                    <span>{{ product.name }}</span>
                </a>
            </li>
        </ul>

        <!-- banner -->
        <div class="banner">
            <img src="https://fuss10.elemecdn.com/3/c8/45b2ec2855ed55d90c45bf9b07abbpng.png?imageMogr/format/webp/thumbnail/!710x178r/gravity/Center/crop/710x178/" alt="">
        </div>
        <!-- 推介商家 -->
        <div id="buseller">— ——推介商家— ——</div>
<<<<<<< HEAD
<<<<<<< HEAD
        
        <div class="">

        </div>

        




=======
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
         <div class="sellerLists clearfix">
            <div class="sellerList clearfix">
                <div class="pic fl" v-for="(item, index) in recommend" :key="item.id">
                    <router-link :to="'/GoodsDetail/' + item.id" tag="li">
                        <img :src="item.avatar" alt="" class="fl">
                        <ul class="conList">
                            <li>
                                <span class="brand">品牌</span>
                                <span class="sell">{{ item.name }}</span>
                                <span class="note fr">票</span>
                            </li>
                            <li>
                                <img src="./img/images/tuijie_03.gif" alt="">
                                <span class="start">{{ item.rating }}</span>
                                <span class="mar">{{item.recent_order_num}}</span>
                            </li>
                            <li>
                                <span class="give">{{ item.give }}</span>   
                                <span class="pai">{{ item.tip }}</span>
                                <span class="km">{{ item.range}}</span>
                                <span>{{ item.time }}</span>
                            </li>
                        </ul>
                        <div class="fullCut">
                            <ul>
                                <li>
                                    {{ item.description}}
                                    <span class="active fr" @click="showFn(index)">{{ index }}个活动</span>
                                </li>
                                <li>
                                    <p>满39减5元</p>
                                    <p id="new_user" v-show="isShow">{{ item.description}}</p>
                                </li>
                            </ul>
                        </div>
                    </router-link> 
                </div> 
            </div>
        </div>
<<<<<<< HEAD
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
    </div>
</template>
    
<script>
export default {
    name: "component_name",
    data () {
        return {
            delicious:[],
<<<<<<< HEAD
<<<<<<< HEAD
            seller:[],
            find:[]
        };
    },
<<<<<<< HEAD
    // created(){
    //     this.$http.get('/api/seller')
    //     .then((res)=>{
    //         this.seller = res.data.data
    //         console.log(res.data.data)
    //     })
    //     this.$http.get('/api/goods')
    //     .then((res)=>{
    //         // console.log(res.data.data)
    //     })
    //     this.$http.get('/api/ratings')
    //     .then((res)=>{
    //         // console.log(res.data.data)
    //     })
        
    // },
    mounted(){
    console.log(this.seller)
=======
=======
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
            recommend:[],
            isShow:false
        };
    },
    methods:{
        showFn(index){
            console.log(index)
            this.isShow =!this.isShow
        }
    },
<<<<<<< HEAD
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
    created(){
        this.$http.get('/api/seller')
        .then((res)=>{
            this.seller = res.data.data
            // console.log(res.data.data)
        })
        this.$http.get('/api/goods')
        .then((res)=>{
            // console.log(res.data.data)
        })
        this.$http.get('/api/ratings')
        .then((res)=>{
            // console.log(res.data.data)
        })
         this.$http.get('/api/delicious')
        .then((res)=>{
            this.delicious = res.data.data
<<<<<<< HEAD
<<<<<<< HEAD
            console.log(res.data.data)
        }) 
         this.$http.get('/api/find')
        .then((res)=>{
            this.find = res.data.data
            console.log(res.data.data)
        }) 
<<<<<<< HEAD
>>>>>>> a0675826edb3203044981ca61e61688bc0d20548
=======
>>>>>>> a0675826edb3203044981ca61e61688bc0d20548
=======
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
            // console.log(res.data.data)
        }) 
        this.$http.get('/api/recommend')
        .then((res)=>{
            this.recommend = res.data.data
            // console.log(res.data.data)
        }) 
<<<<<<< HEAD
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
    }
}
</script>
    
<style lang="css" scoped>
<<<<<<< HEAD
<<<<<<< HEAD
.home img{
    width: 100%;
}
.home p{
    height: 0.5rem;
    font-size: 0.17rem;
    color: #fff;
    text-indent: 0.25rem;
    padding: 0.13rem;
    background: url(./img/header_03.gif) no-repeat 0.2rem center;
    background-color: #0093ff;
}
.home .search{
    height: 0.40rem;
    padding-left:0.1rem;
    font-size: 0.17rem;
    background-color: #0093ff;
}
.home .search input{
    width: 3.53rem;
    height: 0.35rem;
=======
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
.header .address{
    font-size: 0.17rem;
    font-weight: 700;
    color: #fff; 
    text-indent: 0.25rem;
    padding: 0.13rem;
    background: url(./img/header_03.gif)  #00a8ff no-repeat 0.2rem center;
  
}
.header form{
    width: 100%;
    text-align: center;
    padding-top: 0.08rem;
    /* position: relative;ion: fixed;   */
    background: #00a8ff; 
}
.header form input{
    width: 3.5rem;
    height:0.35rem;
<<<<<<< HEAD
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
    text-align: center;
    font-size: 0.15rem;  
    background: url(./img/header_07.gif) no-repeat 0.8rem center;
    background-color: #fff;
}
<<<<<<< HEAD
<<<<<<< HEAD
=======
.header img{
    width: 100%;
}
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
.header img{
    width: 100%;
}
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
/*kind  */
.kind{
    padding: 0 0.17rem;
}
.kind li{
    width: 20%;
    text-align: center;
} 
.kind img{
    width: 0.4rem;
    vertical-align: top;
}
.kind span{
    display:block;
    font-size: 0.12rem; 
}
/* banner */
.banner{
    text-align: center;
}
.banner img{
    width: 3.55rem;
    height: 0.89rem;
    margin-top: 0.1rem;
}
/* 推介商家 */
#buseller{
    height: 0.5rem;
    line-height: 0.5rem;
    text-align: center;
    font-size: 0.14rem;
<<<<<<< HEAD
<<<<<<< HEAD
    color:#000;
}
=======
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
}
/* 商家列表部分 */
.sellerLists{
    width: 100%;
    padding: 0.1rem;
}
.sellerList .pic{
    padding: 0.03rem 0.1rem 0.1rem 0;
    border-bottom:1.5px dotted #ccc;
}
.sellerLists .sellerList img{
    width: 0.75rem;
    margin-top: 0.05rem;
    margin-right: 0.08rem;  
}
.sellerList .conList{
    overflow: hidden;
}
.sellerList .conList span{
    font-size: 0.1rem;
    color: #666666;
}
.sellerList .conList .note{
    padding-left:0.4rem;
    margin-top: 0.07rem;
   
}
.sellerList .conList .brand{
    display: inline-block;
    width: 0.4rem;
    height: 0.2rem;
    background: #ffe924;
    vertical-align: middle;
    text-align: center;
}
.conList .icon-close::before {
    color:red;
    margin-right:0.1rem;
}
.sellerList .conList .sell{
    padding-left: 0.2rem;
    font-size: 0.16rem;
    font-weight: bold;
    color: #333333;
}
.sellerList .conList .start{
    padding-left: 0.2rem;
}
.sellerList .conList .give,
.sellerList .conList .km{
    padding-right: 0.05rem;
    border-right: 1px solid #ccc;
}
.sellerList .conList .pai{
    margin-right: 0.1rem;
}
.sellerLists .fullCut{
    padding-left: 1rem; 
    font-size: 0.12rem;
    color: #666;
}  




<<<<<<< HEAD
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd




</style>