<template>
   <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em buca de novas oportunidades.</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
        <li>Java</li>
        <li>Php</li>
        <li>Javascript</li>
        <li>Css</li>
    </ul>
    <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
  </div>
</template>

<script>
   export default{
      name: 'Info',
      data(){
         return{
            esta_trabalhando: false,
            mostrar_email: true,
            email: "Leandrodossantos.lc5@gmail.com"
         }
      }
   }
</script>