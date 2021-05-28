<template>
  <div class="header">
    <div class="header__container">
      <div class="header__container__lefth"><h1>Clientes Table</h1></div>
      <div class="header__container__center">
        <a @click="mudarModal">Cadastrar</a>
        <a>Conhecer</a>
        <a>Apoiar</a>
      </div>
      <div class="header__container__right"><a>Login</a></div>
    </div>
    <div v-if="desativar" class="modal">
      <div v-if="desativar" class="modal__two">
        <Modal :modal-top="mudarModal" />
      </div>
    </div>
  </div>
</template>
<script>
import Modal from "@/components/Modal";
export default {
  data() {
    return {
      desativar: false,
    };
  },
  components: {
    Modal,
  },
  methods: {
    mudarModal() {
      this.desativar = !this.desativar;
    },
  },
};
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 60px;
  background: #303030;
  display: flex;
  justify-content: center;
  &__container {
    width: 100%;
    max-width: 1170px;
    height: 60px;
    display: flex;
    justify-content: space-between;
    &__lefth {
      width: 45%;
      height: 100%;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      h1 {
        color: rgb(41, 4, 252);
      }
    }
    &__center {
      width: 45%;
      height: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      a {
        color: rgb(41, 4, 252);
        cursor: pointer;
      }
    }
    &__right {
      width: 45%;
      height: 100%;
      display: flex;
      justify-content: flex-end;
      align-items: center;
      a {
        color: rgb(41, 4, 252);
        font-size: 36px;
        cursor: pointer;
      }
    }
  }
}
.modal {
  width: 100%;
  height: 100%;
  background: rgb(0, 0, 0, 0.8);
  top: 0;
  left: 0;
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  &__two {
    width: 500px;
    height: 300px;
    background: #303030;
    border-radius: 5px;
  }
}
</style>
