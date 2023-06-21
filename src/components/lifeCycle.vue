<template>
 <h1>Meu nome é: {{nome}} </h1>
</template>

<script>

export default {
 name: "lifeCycle",
 data() {
  return {
   nome: "Ainda n sei"
  }
 },
 created(){
  setTimeout(() => {
   this.nome = "Ekson"
  }, 1000);
 },
 mounted(){
  setTimeout(() => {
   this.nome = "Pedro"
  }, 2000);
 }
}
</script>
