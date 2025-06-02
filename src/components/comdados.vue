<template> 
    <div>
        <h1>Componente com Dados</h1>
        <p>Nome: {{ nome2 }} - {{ codigo }} </p>
    </div>
</template>

<style scoped>
div {
    background-color: #4caf50;
    padding: 10px;
    margin: 30px;
    border: 2px solid #388e3c;
    border-radius: 15px;
    text-align: center;
}

</style>

<script setup>
const nome2 = 'Lapiseira';
        const codigo = '#125';
</script>

<!--<script>
    options API
export default {
    data: function() {
        return {
            nome: 'Caderno',
            codigo: '#123'
        }
    }
}

 Composition API
export default {
    setup: function() {
        const nome = 'Borracha';
        const codigo = '#123';

        return { nome, codigo };
    }
}
</script>-->

