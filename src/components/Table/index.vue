<template>
  <div class="container">
    <h1>{{ cliente.nome }}</h1>
    <p>{{ cliente.email }}</p>
    <p>{{ cliente.idade }}</p>
  </div>
</template>
<script>
export default {
  props: {
    nome: String,
    email: String,
    idade: Number,
    cliente: Object,
  },
};
</script>

<style lang="scss" scoped>
.container {
  width: 250px;
  height: 250px;
  background: #303030;
  padding: 10px;
  margin: 0 10px 15px 0;
  border-radius: 4px;
}
</style>
