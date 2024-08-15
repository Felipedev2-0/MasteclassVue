<template>
  <div class="componente">
    <h1>Componente com Dados Reativos Primitivos</h1>
    <p>Nome: {{ nome }} | Idade: {{ idade }} </p>
    <!--v-on ou @click é a mesma coisat-->
    <button v-on:click="fazerAniversario()">Fazer Aniversário</button>
    <button @click="mudarNome()">Mudar Nome</button>
  </div>
</template>

<script setup>
import {ref} from "vue"
    const nome = ref("Felipe");
    const idade = ref(31)

    function fazerAniversario() { 
        idade.value += 1
    }

    function mudarNome(){
        nome.value = "Felipe Barros"
    }

</script>

