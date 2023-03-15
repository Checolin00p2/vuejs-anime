<template>
  <div class="hello">
    <h1>Anime</h1>
    <h1>Capitulo: {{ chap + 1 }}</h1>
    <div class="iframe-container">
      <video :src=videom[chap]   controls controlslist="nodownload" autoplay>
        
      </video>
      
      
      
    </div>
    
    <button @click="AfterChap">Anterior</button>
    <input type="number" v-model=newbar @keyup="  chap =newbar-1" placeholder="Numero de Capitulo">
    <button @click="NextChap">Siguiente</button>


  </div>
</template>

<script>

export default {
  components: {
    
  },
  data() {
    return {
      chap: 0,
      newbar:1
    }
  },
  computed: {
    videom() {
      return this.$store.state.temp.cap; // Suponemos que `video` está almacenado en el estado del store de Vuex.
    },
  },
  methods: {
    NextChap() {
      this.chap++
      this.newbar++
      

    },
    AfterChap() {
      this.chap--
      this.newbar--
      
    }
  }
}
</script>




<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.iframe-container {
  height: 75%;
  padding-right: 5%;
  padding-left: 5%;

}

.iframe-container video {
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid #000;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  /* Sombra */
}

button {
  margin: 15px;
}

h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}</style>
