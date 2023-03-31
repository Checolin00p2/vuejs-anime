<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-md-12">
        <nav aria-label="Page navigation example">
          <ul class="pagination pagination-lg justify-content-center" style="width: 100%;">
            <li class="page-item"><button class="page-link text-custom" @click="AfterChap">Anterior</button></li>
            <li class="page-item"><button class="page-link text-custom" disabled >1</button></li>
            <li class="page-item"><button class="page-link text-custom" @click="NextChap" >Siguiente</button></li>
          </ul>
        </nav>
      </div>
    </div>
    <div class="row">
      <div class="col-md-12">
        <video :src="videom[chap]" controls controlslist="nodownload" style="width: 100%;"></video>
      </div>
    </div>
  </div>

</template>


<script>
export default {
  components: {},
  data() {
    return {
      chap: 0,
      newbar: 1,
    };
  },
  computed: {
    videom() {
      //return this.$store.state.temp.cap; // Suponemos que `video` está almacenado en el estado del store de Vuex.
      return this.$store.state.Animes[0].capitulos // Suponemos que `video` está almacenado en el estado del store de Vuex.
    },
  },
  methods: {
    NextChap() {
      this.chap++;
      this.newbar++;
    },
    AfterChap() {
      this.chap--;
      this.newbar--;
    },
  },
};
</script>




<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/*
.iframe-container {
  height: 75vh;
  padding-right: 5%;
  padding-left: 5%;
}

.iframe-container video {
  width: 100%;
  height: 100%;
  border: 2px solid #000;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

.video-container {
  margin-top: 1rem;
  margin-bottom: 1rem;
}
*/
.text-custom {
  font-size: 1.2rem;
  font-family: sans-serif;
  margin-bottom: 1rem;
  color: #000;
}
video{
  border: 1px solid #ffffff; 
  border-radius: 10px;
}



</style>
