<template>
  <div class="colaps">
    <div class="colaps__container">
      <div :class="{ one: !mudar1, two: mudar1 }">
        <div class="title">
          <span>perguntas frequentes</span>
          <a @click="mudarcolapse1">></a>
        </div>

        <p v-if="mudar1">
          Como faço pra participar do progeto ? somete se cadastrando na barra
          superior.
        </p>
        <hr />
      </div>
      <div :class="{ one: !mudar2, two: mudar2 }">
        <div class="title">
          <span>perguntas frequentes</span>
          <a @click="mudarcolapse2">></a>
        </div>

        <p v-if="mudar2">
          Como faço pra participar do progeto ? somete se cadastrando na barra
          superior.
        </p>
        <hr />
      </div>
      <div :class="{ one: !mudar3, two: mudar3 }">
        <div class="title">
          <span>perguntas frequentes</span>
          <a @click="mudarcolapse3">></a>
        </div>

        <p v-if="mudar3">
          Como faço pra participar do progeto ? somete se cadastrando na barra
          superior.
        </p>
        <hr />
      </div>
      <div :class="{ one: !mudar4, two: mudar4 }">
        <div class="title">
          <span>perguntas frequentes</span>
          <a @click="mudarcolapse4">></a>
        </div>

        <p v-if="mudar4">
          Como faço pra participar do progeto ? somete se cadastrando na barra
          superior.
        </p>
        <hr />
      </div>
      <div :class="{ one: !mudar5, two: mudar5 }">
        <div class="title">
          <span>perguntas frequentes</span>
          <a @click="mudarcolapse5">></a>
        </div>

        <p v-if="mudar5">
          Como faço pra participar do progeto ? somete se cadastrando na barra
          superior.
        </p>
        <hr />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mudar1: false,
      mudar2: false,
      mudar3: false,
      mudar4: false,
      mudar5: false,
    };
  },
  methods: {
    mudarcolapse1() {
      this.mudar1 = !this.mudar1;
      this.mudar2 = false;
      this.mudar3 = false;
      this.mudar4 = false;
      this.mudar5 = false;
    },
    mudarcolapse2() {
      this.mudar2 = !this.mudar2;
      this.mudar1 = false;
      this.mudar3 = false;
      this.mudar4 = false;
      this.mudar5 = false;
    },
    mudarcolapse3() {
      this.mudar3 = !this.mudar3;
      this.mudar2 = false;
      this.mudar1 = false;
      this.mudar4 = false;
      this.mudar5 = false;
    },
    mudarcolapse4() {
      this.mudar4 = !this.mudar4;
      this.mudar2 = false;
      this.mudar3 = false;
      this.mudar1 = false;
      this.mudar5 = false;
    },
    mudarcolapse5() {
      this.mudar5 = !this.mudar5;
      this.mudar2 = false;
      this.mudar3 = false;
      this.mudar4 = false;
      this.mudar1 = false;
    },
  },
};
</script>

<style lang="scss" scoped>
.colpase {
  display: flex;
  border: 1px solid #fff;
  &__container {
    display: flex;
  }
}
.one {
  width: 400px;
  height: 60px;
  border-bottom: 1px solid rgb(128, 124, 124);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.two {
  width: 400px;
  height: 150px;
  border-bottom: 1px solid rgb(128, 124, 124);
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
}
.title {
  width: 400px;
  display: flex;
  justify-content: space-between;
}
span {
  font-size: 32px;
  color: #fff;
}
a {
  color: rgb(41, 4, 252);
  font-weight: bold;
}
</style>
