<template>
  <div id="app">
    <!-- router-view是单页应用，路由切换时填充内容的容器，
      换句话说，就是每点击一个路由跳转，我们只是把router-view中的内容替换掉而已
     -->
    <router-view></router-view>
    <div class="tabbar">
        <router-link to="/home" class="home">
            <img src="./components/component1/img/images/icon_03.gif" alt="外卖">
            <h5>外卖</h5>
        </router-link>
        <router-link to="/find" class="find">
            <img src="./components/component1/img/images/icon_05.gif" alt="发现">
            <h5>发现</h5>
        </router-link>
        <router-link to="/cart" class="cart">
            <img src="./components/component1/img/images/icon_07.gif" alt="订单">
            <h5>订单</h5>
        </router-link>
        <router-link to="/mine" class="mine">
            <img src="./components/component1/img/images/icon_09.gif" alt="我的">
            <h5>我的</h5>
        </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
 
  }
}


</script>

<style>

#app .tabbar{
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  height: 0.5rem;
<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
  background-color: pink;
=======
>>>>>>> a0675826edb3203044981ca61e61688bc0d20548
=======
>>>>>>> a0675826edb3203044981ca61e61688bc0d20548
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
  display: flex;
  align-items: center;
  justify-content: space-around;
  font-size: 0.18rem;
  background: #fff;
}
.tabbar .home,
.tabbar .find,
.tabbar .cart,
.tabbar .mine{
  width: 25%;
  text-align: center;
}
.tabbar img{
  width: 0.15rem;
<<<<<<< HEAD
}
.tabbar .home,
.tabbar .find,
.tabbar .cart,
.tabbar .mine{
  width: 25%;
  text-align: center;
}
.tabbar img{
  width: 0.18rem;
=======
>>>>>>> fdc3bf365503d5f1599ff1abc4d842dff21d1bfd
}


</style>
