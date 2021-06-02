<template>
  <div class="container">
    <h1>{{ cliente.nome }}</h1>
    <p>{{ cliente.email }}</p>
    <p>{{ cliente.idade }}</p>
    <button @click="emitirEventoDelet">Deletar</button>
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
  methods: {
    emitirEventoDelet() {
      console.log("emitindo do filho");
      this.$emit("meDelete", {
        idDoCliente: this.cliente.id,
        curso: "formação de curso js",
        components: this,
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  width: 250px;
  height: 250px;
  background: #303030;
  padding: 20px;
  margin: 0 10px 15px 0;
  border-radius: 4px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  box-shadow: 5px -9px 3px rgb(41, 4, 252);
  button {
    width: 80px;
    height: 30px;
    background: rgb(41, 4, 252);
    border: none;
    border-radius: 4px;
    cursor: pointer;
    &:hover {
      background: rgb(36, 22, 112);
    }
  }
}
</style>
