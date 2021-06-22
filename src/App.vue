<template>
  <Navbar :titulonav="titulo" :serviciosnav="servicios"/>
  <div class="container mt-5 col-sm-6 offset-sm-3">
    <h3 class="text-center">{{ titulo}} - Cuenta </h3>
  <Tabla :saldotabla="saldo" :estadotabla="estado"/>

  <Buton tipo="Agregar Saldo" @accion="agregarSaldo"/>
  <Buton tipo="Disminuir" @accion="disminuirSaldo"/>
  <!-- <Buttonestado :estadobtn="estado" @accionestado="cambiarEstado"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue'
import Tabla from './components/Tabla.vue'
import Buton from './components/Buton.vue'
import Buttonestado from './components/Buttonestado.vue'

export default {
  name: 'App',
  components: {
     Navbar,
     Tabla,
     Buton,
     Buttonestado
  },
  data () {
    return {
      titulo: "Mi banco",
      servicios : ['Prestamos', 'Cuenta Corriente', 'Giros', 'Depósitos'],
      saldo: 2000,
      estado: true,
      fecha: '2021-03-20'
    }
  },
  methods: {
    agregarSaldo() {
      this.saldo = this.saldo + 100
    },
    disminuirSaldo() {
      this.saldo = this.saldo - 100
    },
    cambiarEstado() {
      this.estado? this.estado = false: this.estado = true
    }
  }
}
</script>

<style>

</style>
