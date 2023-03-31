<template>
  <div class="container">
    <NavBar />
    <VideoMedia id="MediaVideo" :ResultadoBusqueda="busqueda"/>
    <!-- <ResultadoAnime /> -->
    <!-- <img src="./assets/background.jpg" alt="J-hope" srcset=""> -->
  </div>
</template>

<script>
import VideoMedia from './components/VideoMedia.vue'
import NavBar from './components/NavBar.vue'
//import ResultadoAnime from './components/ResultadoAnime.vue'
export default {
  name: 'App',
  components: {
    VideoMedia,
    NavBar,
    //ResultadoAnime
  },
  data() {
    return {
      busqueda:'',
    }
  }
};
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
#MediaVideo{
  background: rgba(255, 255, 255, 0.2);
  padding: 20px;
  border-radius: 0 0 15px 15px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}
</style>
