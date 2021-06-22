<template>
  <button :class="colorestado" @click="alternarEstado"> {{ estadobtn ? 'Desactivar': 'Activar'}}</button>
</template>

<script>
export default {
  props: {
    estadobtn: Boolean
  },
  methods: {
    alternarEstado() {
      this.$emit('accionestado')
    }
  },
  computed: {
    colorestado() {
      return this.estadobtn? 'btn btn-warning': 'btn btn-success'
    }
  }
}
</script>

<style>

</style>