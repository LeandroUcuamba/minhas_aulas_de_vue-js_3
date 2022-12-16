<template>
  <form action="" @submit="enviarFormulario($event)">
     <input type="text" v-model="name"/><br>
     <input type="text" v-model="email"/>
     <InputSubmit />
  </form>
</template>

<script>
   import InputText from './form/InputText.vue';
   import InputSubmit from './form/InputSubmit.vue';

   export default{
      name: 'Form',
      components: {
        InputText,
        InputSubmit
      },
      data(){
         return{
            name: "",
            email: ""
         }
      },
      methods: {
         enviarFormulario(e){

            const name = this.name;
            const email = this.email;
             
            e.preventDefault();          
            console.log("Formulario enviado")
            console.log("O nome é:"+" "+name);
            console.log("O email é:"+" "+email)

            //Ajax

            //Inserir no banco de dados
         }
      }
   }
</script>

<style scoped>
   p{
      margin: 150px;
   }
</style>