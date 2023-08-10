<template>
  <div id="painelResumo">
    <div class="resumoCaixa">
        <span class="fraseResumo">Dinheiro em caixa</span>
        <span class="caixa">R$ 0</span>
    </div>
    <div class="graficoComportamento">
      <canvas></canvas>
    </div>
  </div>
</template>

<script>
export default {
  name: "painelResumo"
}
</script>

<style scoped>
#painelResumo {
  width: 60%;
  padding: 10px;
  background-color: white;
  border-radius: 20px;
  margin-top: 10px;
}

.resumoCaixa {
  text-align: right;
  padding: 10px;
}

.resumoCaixa span {
  display: block;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-weight: 700;
}

.fraseResumo {
  font-size: 300%;
}

.caixa {
  font-size: 400%;
}
</style>