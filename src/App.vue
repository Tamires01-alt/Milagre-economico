<template>
  <div>
    <Marca />
    <Header />

    <div id="container">
      <PainelLancamento />
      <painelResumo />
    </div>
  </div>
</template>

<script>
import PainelResumo from './components/painelResumo.vue'
import PainelLancamento from './components/painelLancamento.vue'
import Header from './components/header.vue'
import Marca from './components/marca.vue'

export default {
  name: 'App',
  components: { Marca, Header, PainelLancamento, PainelResumo
  }
}
</script>

<style>
:root {
  --cor-destaque: #5333ed;
}
body {
  margin: 0;
  background-color: #dddddd;
}

#container {
  display: flex;
  padding: 20px;
}
</style>
