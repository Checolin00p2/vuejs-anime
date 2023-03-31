<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
      <a class="navbar-brand" href="#">Anime Pa' Ti</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="#">Animes</a>
          </li>

        </ul>
        <form class="form-inline my-2 my-lg-0" id="search-form">
          <input id="inputcustom" class="form-control  mr-sm-2" type="search" placeholder="Buscar" aria-label="Buscar">
          <button class="btn btn-outline-light my-2 my-sm-0" type="submit">Buscar</button>
        </form>

      </div>
    </div>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
#search-form {
  display: flex;
  align-items: center;
}

#search-form input {
  flex: 1;
}

@media (max-width: 767px) {
  #search-form {
    margin-top: 10px;
  }
}
#inputcustom{
  margin-right: 5px;
}
</style>