<template>
  <div>
     <Header :esta_logado="true" />
     <PrimeiroComponente />
     <p class="paragrafo-pai">O dados da App é: {{testando}}</p>
     <LifeCycle />
     <Pessoa /> 
  </div>
</template>

<script>

import PrimeiroComponente from './components/PrimeiroComponente.vue'; 
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';
import Header from './components/Header.vue';

   export default{
    name: "App",
    components: {
      Header, 
      PrimeiroComponente, 
      LifeCycle, 
      Pessoa 
      },
    data(){
      return{
         testando: "teste"
      }
    }
}
</script>

<style>
    body {
      background-color: #333;
      color: #FFF;
    }

    a{
      color: red;
    }

    .teste{
      background-color: black;
    }
</style>