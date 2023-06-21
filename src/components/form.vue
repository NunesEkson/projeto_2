<template>
<h2>Meu Formulario: </h2>
 <form action="" @click="enviarFormulario($event)">
  <div>
   <input type="text" v-model="name">
  </div>
  <div>
   <input type="text" v-model="email">
  </div>
  <div>
   <Submit/>
  </div>
 </form>
 <p>Conteudo</p>
 <p>Conteudo</p>
 <p>Conteudo</p>
</template>

<script>
//import InputText from './Form/InputText.vue'
import Submit from './Form/Submit.vue'
export default {
 // eslint-disable-next-line vue/multi-word-component-names
 name: 'form',
 components: {
  //InputText,
  Submit
 },
 data(){
  return {
   name: 'Ekson',
   email: 'blablalbla@gmail.com'
  }
 },
 methods: {
  enviarFormulario(e) {
   const name = this.name;
   const email = this.emal;
   e.preventDefault();
   console.log('Formulaio enviado')
   console.log('Meu nome é: ' + name )
   console.log('Meu email é: ' + email)
  }
 }
}
</script>
<style scoped>
p {
 margin: 50px;
}
</style>