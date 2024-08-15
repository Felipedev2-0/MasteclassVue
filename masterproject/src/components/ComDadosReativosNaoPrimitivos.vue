<template>
  <div class="componente">
    <h1>Componente com Dados Reativos NAO Primitivos</h1>
    <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }} </p>
    <!--v-on ou @click é a mesma coisat-->
    <button @click="fazerAniversario()">Fazer Aniversário</button>
    <button @click="mudarNome()">Mudar Nome</button>
  </div>
</template>



<!--COMPOSITION API'S-->
<!--<script setup>
import {reactive} from "vue"
    const pessoa = reactive({nome: "Felipe", idade: 31})

    function fazerAniversario() { 
        pessoa.idade += 1
    }

    function mudarNome(){
        pessoa.nome = "Felipe Albuquerque"
    }

</script> -->


<!--OPTION API-->
<script>
  export default{
    data:function(){
      return{
        pessoa:{
          nome:"Felipe",
          idade:31
        }
      }
    },
    methods:{
      fazerAniversario:function(){
        this.pessoa.idade +=1
      },
      mudarNome: function() { 
        this.pessoa.nome="Felipe Albuquerque"
       }
    }
  }

</script>

