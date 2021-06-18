<template>
  <button :class="colorBoton" @click="accionbtn">{{ tipo }}</button>
</template>

<script>
export default {
  props: {
    tipo: String
  },
  methods: {
    accionbtn () {
      this.$emit('accion')
    }
  },
  computed: {
    colorBoton() {
      return this.tipo === 'Agregar Saldo'? 'btn btn-primary': 'btn btn-danger'
    }
  }
}
</script>

<style>
  button {
    margin-right: 5px !important;
  }
</style>