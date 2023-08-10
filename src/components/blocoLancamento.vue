<template>
  <div class="blocoLancamento">
		<div class="botoes">
			<img
					v-if="tipo === 'entrada'"
					src="../img/mais.png"
					alt="entrada"
					class="ImagemLancamento"
			 />
			 <img
					v-else-if="tipo === 'saida'"
					src="../img/menos.png"
					alt="gastos"
					class="ImagemLancamento"
			 />
				<img src="" alt="" class="imagemLancamento">
				<button class="botaoRemover">
					<img src="" alt="">
				</button>
		</div>

		<div class="descricaoLancamento">
			 <span class="valor">R$</span>
			 <span>Data</span>
			 <span>Descricao</span>
		</div>
  </div>
</template>

<script>
export default {
	name: "BlocoLancamento",
	props: {
		tipo: String,
		lancamento: Object,
	},
};
</script>

<style>

</style>