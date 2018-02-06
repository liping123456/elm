<template>
    <div class="home">
       <h1>附近的房间里的飞机到了就</h1>
       {{seller.name}}
       {{seller.bulletin}} 
    </div>
</template>
    
<script>
export default {
    name: "component_name",
    data () {
        return {
            seller:[]
        };
    },
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
    }
}
</script>
    
<style lang="css" scoped>
    .home h1{
        width:100%;
        height:2rem;
        background:orange;
        text-align:center;
        font-size:0.16rem;
    }

</style>