<template>
  <div class="colapse">
    <div class=" one">
      <div class="title">
        <span>Cliiente</span><a @click="escondertexto">></a>
      </div>
      <div class="description" v-if="esconder">
        <p>
          Lorem Ipsum é simplesmente uma simulação de texto da indústria
          tipográfica e de impressos, e vem sendo utilizado desde o século XVI,
          quando um impressor desconhecido pegou
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      esconder: false,
    };
  },
  methods: {
    escondertexto() {
      this.esconder = !this.esconder;
    },
  },
};
</script>

<style scoped>
.colapse {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.title {
  width: 400px;
  height: 100%;
  padding: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
span {
  color: #fff;
}
a {
  color: #fff;
}

.description {
  width: 50%;
  height: 100%;
  display: flex;
  align-items: center;
}

.one {
  width: 100%;
  height: 60px;
  border-bottom: 1px solid rgb(122, 120, 120);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.two {
  width: 50%;
  height: 60px;
  border-bottom: 1px solid rgb(122, 120, 120);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
