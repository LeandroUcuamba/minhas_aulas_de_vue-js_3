<template>
   <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em buca de novas oportunidades.</p>
    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
        <li v-for="(technology,index) in backend_technologies" v-bind:key="index">
           {{technology}}
        </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para front-end:</p>
    <ul>
        <li v-for="technology in frontend_technologies" :key="technology.id">
           {{technology.language}}
        </li>
    </ul>
    <div>
       <button @click="showEmail">{{textoBotao}}</button>
    </div>
    <p class="teste" v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
    <p>Para acessar o meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
    <Picture />
  </div>
</template>

<script>

import Picture from "./Picture.vue"

   export default{
      name: 'Info',
      components: { Picture },
      data(){
         return{
            esta_trabalhando: false,
            mostrar_email: true,
            email: "Leandrodossantos.lc5@gmail.com",
            meu_link: "https://google.com",
            textoBotao: "Mostrar Email",
            backend_technologies:["Java","PHP","C#" ],
            frontend_technologies:[
               {id:1, language:"HTML"},
               {id:2, language:"CSS"},
               {id:3, language:"JAVASCRIPT"}
            ]
         }
      },
      methods: {
         showEmail() {
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
              this.textoBotao="Mostrar Email";
            }else{
              this.textoBotao="Esconder Email";
            }
         }
      }
   }
</script>

<style>
  .paragrafo-pai{
     color: red;
  }
</style>