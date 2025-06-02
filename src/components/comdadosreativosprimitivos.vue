<template> 
    <div class="componente">
        <h1>Componente com Dados Reativos Primitivos</h1>
        <p>Nome Dev: {{ nome }} - Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversario">Fazer Aniversário</button>
        <button v-on:click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';

// Usando a API de Composição do Vue 3
const nome = ref("João");
const idade = ref(30);

function fazerAniversario() {
    idade.value += 1;
}

function mudarNome() {
    nome.value = 'Maria';  
}
</script>