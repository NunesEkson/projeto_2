<template>
<div>
 <Header/>
 <PrimeiroComponente />
 <p class="paragrafo-pai">O dado do app é: {{ testando }}</p>
 <life-cycle />
 <Pessoa />
</div>

</template>-

<script>
import Header from './components/Header.vue'
import lifeCycle from './components/lifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import PrimeiroComponente from './components/PrimeiroComponente.vue'
 export default {
  name: 'App',
  components: {
   Header,
   PrimeiroComponente,
   lifeCycle,
   Pessoa
  },
  data() {
   return {
    testando: 'testando app'
   }
  }
 }
</script>

<style>
body {
 background-color: #333;
 color: #fff;
}
a {
 color: red
}
.teste {
 background-color: black;
}
</style>
