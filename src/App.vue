<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <img src="./assets/background.jpg" alt="J-hope" srcset="">
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
  margin-top: 60px;
  
  
}
img{
  width: 25%;
  opacity: 0.6;
}
img:hover{
  opacity: 1;
}

</style>
