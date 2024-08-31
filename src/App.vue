<script setup lang="ts">
  // importacoes
  import { reactive } from 'vue';
  import Cabecalho from './componentes/Cabecalho.vue';
  import Corpo from './componentes/Corpo.vue';
  import Roda from './componentes/Roda.vue';

  // reatividade
  const reativos = reactive({
    tarefa: ''
  });
  // 
</script>

<template>
  <!--  -->
  <header>
    <Cabecalho></Cabecalho>
  </header>
  <main>
    <Corpo></Corpo>
  </main>
  <footer>
    <Roda></Roda>
  </footer>
  <!--  -->
</template>

<style scoped lang="scss">
  /*  */
  header{
    // background-color: red;
  }

  main{
    // background-color: blue;
    // faz com que o main ocupe todo espaco disponivel
    flex-grow: 1;
  }

  footer{
    // background-color: green;
  }
  /*  */
</style>
