<template>
 <ul>
  <li><a href="#">Home</a></li>
  <li><a href="#">Projetos</a></li>
  <li><a href="#">Contato</a></li>
 </ul>
</template>

<script>
export default {
 // eslint-disable-next-line vue/multi-word-component-names
 name: 'Header'
 
}
</script>

<style scoped>
 ul {
  list-style: none;
  display: flex;
  background-color: #111;
 }
 li {
  margin-right: 10px;
 }
 a {
  color: #ddd;
  text-decoration: none;
  transition: .5s;
 }
 a:hover {
  color: turquoise
 }
</style>