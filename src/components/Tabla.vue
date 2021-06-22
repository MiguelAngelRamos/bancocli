<template>
  <table width="300" class="table">
    <thead>
      <tr>
        <th scope="col">Saldo</th>
        <th scope="col">Estado</th>
        <th></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td :class="colorSaldo">{{ saldotabla }}</td>
        <td>{{ estadotabla ? 'Activo': 'Desactivada'}}</td>
        
        <td>
          <div class="form-check form-switch">
            <input
              class="form-check-input"
              type="checkbox"
              id="flexSwitchCheckChecked"
              @click="capturando()"
              v-model="estadotabla"
              checked
            />
          </div>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  props: {
    saldotabla: Number,
    estadotabla: Boolean,
  },
  methods: {
    capturando(e) {
      // console.log(e.target.value)
      // console.log(e.target.indeterminate)
      console.log(this.estadotabla)
    }
  },
  computed: {
    colorSaldo() {
      return this.saldotabla > 500 ? "text-success" : "text-danger";
    },
  },
};
</script>

<style>
 td {
  max-width: 50px;
  font-size: 17px;
}
</style>
