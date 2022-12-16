<template>
  <h1>Olá Vue!</h1>
  <p>O meu nome é {{nome}} e a minha profissao é {{profissao}}</p>
</template>

<script>
   export default{
      name: 'PrimeiroComponente',
      data(){
         return{
           nome: "Leandro",
           profissao: "Programador"
         }
      }
   }
</script>