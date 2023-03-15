<template>
  <div class="container">
    <NavBar />
    <VideoMedia msg="Welcome to Your Vue.js App"/>
    <img src="./assets/background.jpg" alt="J-hope" srcset="">
  </div>
</template>

<script>
import VideoMedia from './components/VideoMedia.vue'
import NavBar from './components/NavBar'
export default {
  name: 'App',
  components: {
    VideoMedia,
    NavBar
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
img{
  width: 25%;
  opacity: 0.6;
}
img:hover{
  opacity: 1;
}

</style>
