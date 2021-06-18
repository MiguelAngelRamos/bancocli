<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">{{ titulonav }}</a>
    <div class="collapse navbar-collapse" id="navbarNav">

      <ul class="navbar-nav">
        <li class="nav-item" v-for="(servicio, index) in serviciosnav" :key="index">
          <a class="nav-link active" aria-current="page">{{ servicio }}</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  props: {
    titulonav: String,
    serviciosnav: Array
  }

}
</script>

<style>

</style>