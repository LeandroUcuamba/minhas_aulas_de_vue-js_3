<template>
  <div>
     <Reutilizacao />
     <h1>Olá Vue!</h1>
     <p>O meu nome é {{nome}} e a minha profissao é {{profissao}}</p>
     <MultiplosEventos />
     <Reutilizacao />
     <Reutilizacao />
     <Reutilizacao />
  </div>
</template>

<script>
   
   import MultiplosEventos from "./MultiplosEventos.vue";
   import Reutilizacao from "./Reutilizacao.vue";

   export default{
      name: 'PrimeiroComponente',
      components:{
         MultiplosEventos,
         Reutilizacao
      },
      data(){
         return{
           nome: "Leandro",
           profissao: "Programador"
         }
      }
   }
</script>