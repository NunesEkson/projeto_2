<template>
 <div>
  <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
  <Info :email='email'/>
  <Form />
 </div>
</template>

<script>
import Info from './Info.vue'
import Form from './form.vue'

export default {
 // eslint-disable-next-line vue/multi-word-component-names
 name: 'Pessoa',
 components: {
  Info,
  Form
 },
 data() {
  return {
   nome: "Ekson",
   email: 'ekson@gmail.com'
  }
 }

}
</script>
