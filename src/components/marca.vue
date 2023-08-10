<template>
  <div>
    <img src="../img/logo.png" >
     <span>tamires</span>
  </div>
</template>

<script>
export default {
  name: "MarcaGrande"

}
</script>

<style scoped>
  div {
    background-color: white;
    padding: 10px;
  }

  img {
    width: 50px ;
    vertical-align: middle;
    margin-left: 10px;
  }
  span {
    color: var(--cor-destaque);
    font-size: 120%;
    font-weight: 600;

  }
</style>