<template>
   <img :src="avatar" :alt="descricao" />
   <MudarImagem @mudar-Imagem="trocarImagem" />
</template>

<script>

  import MudarImagem from "./MudarImagem.vue";

   export default{
      name: 'Picture',
      components:{
         MudarImagem
      },
      data() {
        return{
            avatar: "/img/leo.png",
            descricao: "LeandroUcuamba"
        }
      },
      methods:{
         trocarImagem(){
            this.avatar = "/img/ucuamba.png"
         }
      }
   }
</script>