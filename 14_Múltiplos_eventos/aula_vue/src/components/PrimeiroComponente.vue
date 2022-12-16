<template>
  <h1>Olá Vue!</h1>
  <p>O meu nome é {{nome}} e a minha profissao é {{profissao}}</p>
  <MultiplosEventos />
</template>

<script>
   
   import MultiplosEventos from "./MultiplosEventos.vue";

   export default{
      name: 'PrimeiroComponente',
      components:{
         MultiplosEventos
      },
      data(){
         return{
           nome: "Leandro",
           profissao: "Programador"
         }
      }
   }
</script>