<template>
  <div class="home">
    <Header :modal-teste="keyModal" />
    <div class="home__container">
      <div class="home__container__lefth">
        <div v-for="cliente in clientes" :key="cliente.id">
          <Table :cliente="cliente" @meDelete="deletarUsuario" />
        </div>
      </div>
      <div class="home__container__right">
        <Colapse />
        <Modal :modal-teste="closeModal" v-if="closeModal">
          <div class="modal">
            <a @click="keyModal">fechar</a>
            <input
              type="text"
              placeholder="diigite seu nome"
              v-model="nomeField"
            />
            <input
              type="text"
              placeholder="diigite seu e-mail"
              v-model="emailField"
            />
            <input
              type="text"
              placeholder="diigite seu idade"
              v-model="idadeField"
            />
            <button @click="cadastrar">cadastrar</button>
          </div>
        </Modal>
      </div>
    </div>
  </div>
</template>

<script>
import Table from "@/components/Table";
import Header from "@/components/Header";
import Colapse from "@/components/Colapse";
import Modal from "@/components/Modal";

export default {
  name: "Home",
  components: {
    Header,
    Table,
    Colapse,
    Modal,
  },
  data() {
    return {
      closeModal: false,
      deuErro: false,
      idadeField: 0,
      nomeField: "",
      emailField: "",
      clientes: [
        {
          id: 1,
          nome: "Mario Porto",
          email: "Marioporto@gmail.com",
          idade: 12,
        },
        {
          id: 2,
          nome: "Daniel Silva",
          email: "danielsilva@gmail.com",
          idade: 22,
        },
      ],
    };
  },
  methods: {
    cadastrar() {
      if (
        this.nomeFielde == "" ||
        this.nomeField == " " ||
        this.nomeField < 3
      ) {
        // deuErro = true;
        alert("Senha não são iguais");
      } else
        this.clientes.push({
          nome: this.nomeField,
          email: this.emailField,
          idade: this.idadeField,
          id: Date.now(),
        })(
          ((this.nomeField = ""), (this.emailField = ""), (this.idadeField = 0))
        );
    },
    deletarUsuario: function($event) {
      console.log("recebemdo evento");
      console.log($event.idDoCliente);
      var id = $event.idDoCliente;
      var novoArray = this.clientes.filter((clientes) => cliente.id != id);
      this.clientes = novoArray;
    },
    keyModal() {
      this.closeModal = !this.closeModal;
    },
  },
};
</script>

<style lang="scss" scoped>
.home {
  width: 100%;
  height: 100%;
  background: rgb(94, 93, 93);
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: column;
  &__container {
    width: 100%;
    max-width: 1170px;
    height: 100%;
    display: flex;
    justify-content: space-between;
    &__lefth {
      width: 50%;
      padding-top: 30px;
      display: flex;
      flex-wrap: wrap;
    }
    &__right {
      width: 50%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      input {
        width: 400px;
        height: 30px;
        border-radius: 4px;
        border: none;
        text-align: center;
        margin: 10px;
      }
      button {
        width: 80px;
        height: 30px;
        background: rgb(41, 4, 252);
        border: none;
        border-radius: 4px;
      }
      p {
        color: red;
      }
    }
  }
}
.modal {
  display: flex;
  flex-direction: column;
  a {
    color: #fff;
    width: 80px;
    height: 30px;
    background: red;
    cursor: pointer;
    border-radius: 4px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
