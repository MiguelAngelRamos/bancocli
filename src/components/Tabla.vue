<template>
  <table class="table">
  <thead>
    <tr>
      <th scope="col">Saldo</th>
      <th scope="col">Estado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td :class="colorSaldo">{{ saldotabla }}</td>
      <td v-if="estadotabla">Activo</td>
      <td v-else>Desactivada</td>
    </tr>

  </tbody>
</table>
</template>


<script>
export default {
 props: {
   saldotabla: Number,
   estadotabla: Boolean
 },
 computed: {
   colorSaldo() {
     return this.saldotabla > 500 ? 'text-success': 'text-danger'
   }
 }
}
</script>

<style>

</style>