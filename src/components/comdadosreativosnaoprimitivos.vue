<template> 
    <div class="componente">
        <h1>Componente com Dados Reativos Não Primitivos</h1>
        <p>Nome Dev: {{ pessoa.nome }} - Idade: {{ pessoa.idade }}</p>
        <button @click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<!--<script setup>
import { reactive } from 'vue';

const pessoa = reactive({
    nome: "João",
    idade: 30
});

function fazerAniversario() {
    pessoa.idade += 1;
}

function mudarNome() {
    pessoa.nome = 'Maria';  
}

</script>-->

<script>
export default {
    name: 'ComDadosReativosNaoPrimitivos',
    data() {
        return {
            pessoa: {
                nome: "João",
                idade: 30
            }
        };
    },
    methods: {
        fazerAniversario() {
            this.pessoa.idade += 1;
        },
        mudarNome() {
            this.pessoa.nome = 'Maria';  
        }
    }
};
</script>