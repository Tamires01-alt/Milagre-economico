<template>
  <div class="blocoLancamento">
		<div class="botoes">
			<img
					:src=" tipo === 'entrada' ? mais : menos"
					alt=" tipo === 'entrada' ? 'Entrada' : 'Gasto'"
					class="ImagemLancamento"
			/>
				<button
          @click="excluirLancamento(lancamento.id)"
          class="botaoRemover">
					<img src="../img/lixeira.png" alt="">
				</button>
		</div>

		<div class="descricaoLancamento">
			<span :class="tipo === 'entrada' ? 'valor entrada' : 'valor gasto'"
      >R$ {{ 
        lancamento.valor.toLocaleString(undefined, {
          minimumFractionDigits: 2,
        }) 
      }}</span
      >
			<span>{{ new Date(lancamento.data).toLocaleDateString( "pt-BR", {
        timeZone: "UTC",
      })
    }}</span>
			<span>{{ lancamento.descricao }}</span>
		</div>
  </div>
</template>

<script>
import { mapActions } from 'vuex';
import mais from '../img/mais.png'
import menos from '../img/menos.png'
export default {
	name: "BlocoLancamento",
  data: () => {
    return {
      mais,
      menos,
    };
  },
  methods: mapActions(["excluirLancamento"]),
	props: {
		tipo: String,
		lancamento: Object,
	},
};
</script>

<style scoped>
 .blocoLancamento {
  display: flex;
  background-color: white;
  border-radius: 20px;
  padding: 10px;
  margin-bottom: 10px;
 }

 .botoes {
  width: 50%;
 }

 .ImagemLancamento {
  width: 50px;
  vertical-align: middle;
  cursor: pointer;
 }

 .botaoRemover{
  border: none;
  outline: none;
  background-color: white;
  vertical-align: middle;
 }

 .botaoRemover:hover{
  cursor: pointer;
 }

 .botaoRemover img{
   width: 40px;
 }

 .botaoRemover img:active{
   filter: invert(100%);
 }
 .descricaoLancamento {
  width: 50%;
  float: right;
  text-align: right;
 }

 .descricaoLancamento span {
   display: block;
   font-size: 80%;
 }

 .valor {
  font-family: 'Courier New', Courier, monospace;
  font-size: 200% !important;
  font-weight: 700;
 }

 .entrada {
  color: #22a7f0
 }
 .gasto {
  color: red;
 }
</style>