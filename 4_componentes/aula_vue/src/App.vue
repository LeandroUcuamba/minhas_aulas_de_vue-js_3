<template>
  <PrimeiroComponente />
</template>

<script>

import PrimeiroComponente from './components/PrimeiroComponente.vue'; 

   export default{
    name: "App",
    /* Tem que especificar o componente pk no arquivo "js" somente esta sendo   
    o "App.vue" */
    components: { PrimeiroComponente }
}
</script>