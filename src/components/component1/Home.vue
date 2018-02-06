<template>
    <div class="home">
        <!-- 头部 -->
        <div class="header">
            <p class="address">上地信息产业基地</p>
            <div class="search">
                <input type="search" placeholder="搜索商家、商品名称">
            </div>
            <img src="https://fuss10.elemecdn.com/0/cf/e16c1687a4ea84674d5b531623934png.png?imageMogr/format/webp/thumbnail/!750x210r/gravity/Center/crop/750x210/" alt="">
        </div>
        
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
        
        <div class="">

        </div>

        




    </div>
</template>
    
<script>
export default {
    name: "component_name",
    data () {
        return {
            delicious:[],
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
    }
}
</script>
    
<style lang="css" scoped>
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
    text-align: center;
    font-size: 0.15rem;  
    background: url(./img/header_07.gif) no-repeat 0.8rem center;
    background-color: #fff;
}
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
    color:#000;
}




</style>