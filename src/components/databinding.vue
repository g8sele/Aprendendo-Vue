<template>
    <div class="componente">
        <h1>Data Binding</h1>
        
        <p>Valor: {{ valor }}</p>
        <!-- <input type="text" v-bind:value="valor"></input>-->

        <!--<input type="text" v-bind:value="valor"
        v-on:input="(e) => valor = e.target.value"
        ></input>-->

        <!-- <input type="text" v-bind:value="valor"
        @input="(e) => valor = e.target.value"
        ></input> -->

        <input type="text" v-model="valor"></input>

    </div>
</template>

<script setup>
import {ref} from 'vue';
const valor = ref('Vue é legal!');
</script>