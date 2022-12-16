<template>
  <div>
     <PrimeiroComponente />
     <p>O dados da App é: {{testando}}</p>
     <LifeCycle />
  </div>
</template>

<script>

import PrimeiroComponente from './components/PrimeiroComponente.vue'; 
import LifeCycleVue from './components/LifeCycle.vue';
import LifeCycle from './components/LifeCycle.vue';

   export default{
    name: "App",
    components: { PrimeiroComponente, LifeCycle },
    data(){
      return{
         testando: "teste"
      }
    }
}
</script>