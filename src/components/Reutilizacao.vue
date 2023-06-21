<template>
 <button @click="ativar">Clique Aqui </button>
 <span v-show="ativou">Ativou!</span>
</template>

<script>

export default {
 // eslint-disable-next-line vue/multi-word-component-names
 name: 'Reutilizacao',
 data() {
  return {
   ativou: false
  }
 },
 methods: {
  ativar() {
   this.ativou = !this.ativou
  }
 }
}
</script>
