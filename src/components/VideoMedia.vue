<template>
  <div class="row">
    <h1>Anime</h1>

    <div class="iframe-container">
      <nav aria-label="Page navigation example">
        <div class="">
          <ul class="pagination row">
            <div class="row">
              <li class="page-item col-1">
                <button class="page-link text-dark" @click="AfterChap">Anterior</button>
              </li>
              <div  class="page-link col-10 text-custom"><h3 class="text-custom">{{chap+1}}</h3></div>
              <li class="page-item col-1">
                <button class="page-link text-dark" @click="NextChap">Siguiente</button>
              </li>
            </div>
          </ul>
        </div>
      </nav>

      <video :src="videom[chap]" controls controlslist="nodownload"></video>
    </div>

    <input
      type="number"
      v-model="newbar"
      @keyup="chap = newbar - 1"
      placeholder="Numero de Capitulo"
    />
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
      return this.$store.state.temp.cap; // Suponemos que `video` está almacenado en el estado del store de Vuex.
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
.text-custom{
  margin: 0;
  padding: 0;
  color: #000;
}

</style>
