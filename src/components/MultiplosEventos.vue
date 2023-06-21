<template>
 <div>
  <button @click="primeiro('Primeiro evento'), segundo('Segundo evento')">Ativar Multiplos Eventos</button>
  <p>{{multiplos_eventos}}</p>
 </div>
</template>

<script>
export default {
 name: 'MultiplosEventos',
 data(){
  return {
   multiplos_eventos: ''
  }
},
methods: {
 primeiro(txt){
  this.multiplos_eventos = txt
 }, 
 segundo(txt){
  setTimeout(() => this.multiplos_eventos = txt, 500)
 }
}
}

</script>

<style scoped>
div {
 margin: 100px;
}
</style>