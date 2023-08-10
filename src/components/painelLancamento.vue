<template>
  <div id="painelLancamento">
    <div id="FormularioLancamento">
        <form>
          <div id="tiposLancamentos">
            <input type="radio" name="tipo" id="entrada">
            <label for="entrada"> Entrada </label>
            <input type="radio" name="tipo" id="saida">
            <label for="saida"> Saida </label>
          </div>

          <label for="valor">Valor</label>
          <input type="number" name="valor" id="valor">
          <label for="descricao">Descricao</label>
          <input type="text" name="descricao" id="descricao">
          <label for="data">Data</label>
          <input type="date" name="data" id="data">
          <button>lancar</button>
        </form>
    </div>
  </div>
</template>

<script>
export default {
    name: "PainelLancamento"

}
</script>

<style scoped>
#painelLancamento {
    width: 40%;
    padding: 20px;
}

#FormularioLancamento {
    background-color: white;
    border-radius: 20px;
    padding: 10px;
}

#valor,
#descricao, 
#data,
button {
  display: block;
  margin-bottom: 10px;
}

#valor,
#descricao,
#data {
  height: 20px;
  font-size: 100%;
}

#tiposLancamento {
  margin-bottom: 10px;
}

#tiposLancamento label {
  margin-right: 20px;
}

#tiposLancamento label:first-of-type {
  color: #22a7f0;
}

#tiposLancamento label:last-of-type {
  color: red;
}
#descricao {
  width: 70%;
}

button {
  background-color: var(--cor-destaque);
  border: none;
  outline: none;
  border-radius: 5px;
  padding: 10px 20px;
  color: white;
  font-size: 120%;
  font-weight: 700;
  cursor: pointer;
}
</style>