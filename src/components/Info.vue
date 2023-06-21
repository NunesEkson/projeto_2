<template>
 <div>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p>Utilizo as seguintes tecnologias para front: </p>
  <ul>
   <li v-for="(tec, index) in tec_front" v-bind:key="index">{{ tec }}</li>
  </ul>
  <p>Aqui estão as tecnoligas para back: </p>
  <ul>
   <li v-for="tec in tec_back" :key="tec.id">{{ tec.language}}</li>
  </ul>
  <div>
   <button @click="showEmail"> {{textoBotao}} </button>
  </div>
  <p v-show="mostrar_email">Mande uma msg para: {{ email }}</p>
  <p class="teste">Para acessar meu portfolio <a v-bind:href="meu_link">basta clicar aqui</a></p>
  <Picture/>
 </div>
</template>

<script> 
import Picture from './Picture.vue'
 export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'info',
  components: {
   Picture
  },
  props: {
   email: String
  },
  data() {
   return {
    esta_trabalhando: false,
    mostrar_email: false,
    meu_link: 'https://google.com',
    textoBotao: 'Mostrar email',
    tec_front: ['JavaScript', 'HTML', 'CSS', 'Vue3'],
    tec_back: [
     {id: 1, language: 'Python'},
     {id: 2, language: 'Java'},
     {id: 3, language: 'PHP'}
    ]
   }
  },
  methods:{
   showEmail(){
    this.mostrar_email = !this.mostrar_email
    if(!this.mostrar_email){
     this.textoBotao = 'Mostrar email'
    } else {
     this.textoBotao = 'Esconder email'
    }
   }
  }
 }
</script>

<style>

</style>