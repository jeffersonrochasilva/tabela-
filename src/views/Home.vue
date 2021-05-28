<template>
  <div class="home">
    <Header />
    <div class="home__container">
      <div class="home__container__lefth">
        <Table :cliente="clienteVictor" />
        <Table :cliente="clienteJoao" />
        <Table :cliente="clienteGustavo" />
        <Table :cliente="clienteMaria" />
      </div>
      <div class="home__container__right">
        <Colapse />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Table from "@/components/Table";
import Header from "@/components/Header";
import Colapse from "@/components/Colapse";

export default {
  name: "Home",
  components: {
    Header,
    Table,
    Colapse,
  },
  data() {
    return {
      clienteVictor: {
        nome: "Victor Lima",
        email: "victor@gmail.com",
        idade: 22,
      },
      clienteMaria: {
        nome: "Maria Silva",
        email: "mariasilva@gmail.com",
        idade: 32,
      },
      clienteJoao: {
        nome: "João Albuqueruqe",
        email: "albuquerque@gmail.com",
        idade: 18,
      },
      clienteGustavo: {
        nome: "Gustavo andrade",
        email: "gustavoandrade@gmail.com",
        idade: 27,
      },
    };
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
      justify-content: flex-end;
      align-items: center;
    }
  }
}
</style>
