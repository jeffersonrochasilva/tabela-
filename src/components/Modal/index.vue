<template>
  <div class="modal">
    <input type="text" placeholder="Digite seu nome" />
    <input type="text" placeholder="Digite seu e-mail" />
    <input type="text" placeholder="Digite sua idade" />
    <button @click="modalTop">Cadastrar</button>
  </div>
</template>
<script>
export default {
  props: {
    modalTop: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.modal {
  width: 500px;
  height: 300px;
  // position: fixed;
  display: flex;
  justify-content: space-around;
  flex-direction: column;
  input {
    width: 400px;
    height: 30px;
    border-radius: 4px;
    margin: 25px;
    text-align: center;
    border: none;
  }
  button {
    width: 100px;
    height: 30px;
    background: rgb(41, 4, 252);
    border: none;
    border-radius: 4px;
    cursor: pointer;
    color: #fff;
    &:hover {
      background: rgb(99, 73, 248);
    }
  }
}
</style>
