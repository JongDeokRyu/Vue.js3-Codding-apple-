<template>
  <img alt="Vue logo" src="./assets/logo.png">

  <div class="menu">
    <a v-for="(menu , index) in 메뉴들" :key="index">{{ menu }}</a>
  </div>
<!-- 
  <div>
    <h4 :style="testStyle"> {{ products[0] }}</h4>
    <p>{{ price1 }} 만원</p>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }} 만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>가격은 아무거나</p>
  </div> -->

  <div v-for="(product , index) in products" :key="index">
    <h4> {{ products[index] }}</h4>
    <p> XX 만원 </p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      price1 : 60,
      price2 : 70,
      products : ['역삼동원룸' , '천호동원룸' , '마포구원룸'],
      testStyle : 'color : blue',
      메뉴들 : ['Home' , 'Shop' , 'About'],
    }
  },//데이터 보관함
  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background : darkslateblue;
  padding : 15px;
  border-radius: 5px;
}

.menu a {
  color : white;
  padding : 10px;
}

</style>
