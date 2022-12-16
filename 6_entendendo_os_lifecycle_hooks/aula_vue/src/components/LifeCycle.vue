<template>
  <h1>Meu nome é: {{nome}}</h1>
</template>

<script>
  export default{
    name: "LifeCycle",
    data(){
       return{
         nome: "Ainda não sei"
       }
    },
    // Aqui estão os eventos LifeCycle_Hook !
    //Ele troca um dado sem precisar regarregar a pagina. "Tipo AJAX";
    created(){
        //Podemos add um metodo setTimeout dentro;
        setTimeout(()=> {
            this.nome = "Leandro"
        }, 2000);

        this.LifeCycle()
    },
    mounted(){
        setTimeout(()=> {
            this.nome = "Ucuamba"
        }, 4000);

        this.LifeCycle()
    },
    //Add apois a aula 10;
    methods: {
       LifeCycle(){
          console.log("Executou");
       }
    }
  }
</script>