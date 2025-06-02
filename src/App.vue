<script setup>
import PrimeiroComponente from "./components/PrimeiroComponente.vue";

import ComDados from "./components/comdados.vue";

import ComDadosReativosPrimitivos from "./components/comdadosreativosprimitivos.vue";

import ComDadosReativosNaoPrimitivos from "./components/comdadosreativosnaoprimitivos.vue";

import DataBinding from "./components/databinding.vue";

import ComProps from "./components/comprops.vue";

import EscutaEvento from "./components/EscutaEvento.vue";

import PropriedadesComputadas from "./components/propriedadescomputadas.vue";

import PropriedadesAssistidas from "./components/propriedadesassistidas.vue";

import RenderizacaoCondicional from "./components/renderizacaocondicional.vue";

import RenderizacaoListas from "./components/renderizacaolistas.vue";

import Slots from "./components/slots.vue";

// Dados para o componente RenderizacaoListas
const cachorrosDoJoao = [
  { nome: 'Rex', idade: 5 },
  { nome: 'Fido', idade: 3 },
  { nome: 'Bobby', idade: 2 }
];

</script>

<template>
<header>Vue</header>
  <PrimeiroComponente />

  <Slots>
    <template v-slot:icone>
    <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="currentColor"  class="icon icon-tabler icons-tabler-filled icon-tabler-home">
    <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
    <path d="M12.707 2.293l9 9c.63 .63 .184 1.707 -.707 1.707h-1v6a3 3 0 0 1 -3 3h-1v-7a3 3 0 0 0 -2.824 -2.995l-.176 -.005h-2a3 3 0 0 0 -3 3v7h-1a3 3 0 0 1 -3 -3v-6h-1c-.89 0 -1.337 -1.077 -.707 -1.707l9 -9a1 1 0 0 1 1.414 0m.293 11.707a1 1 0 0 1 1 1v7h-4v-7a1 1 0 0 1 .883 -.993l.117 -.007z" 
    /></svg>
    </template>
    <template v-slot:texto>
     Home
    </template>
  </Slots>

  <RenderizacaoListas nome="João" :cachorros="[]" />
  <RenderizacaoCondicional nome="João" :qtdeCachorros="5" />
  <PropriedadesAssistidas />
  <PropriedadesComputadas />
  <EscutaEvento />
  <ComDadosReativosPrimitivos />
  <ComDadosReativosNaoPrimitivos />
  <ComDados />
  <DataBinding /> 
  <ComProps item="Notebook" v-bind:preco="2.50" />
</template>


