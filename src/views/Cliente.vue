<template>
  <div class="cliente">
    <Header />
    <div class="cliente__colapse">
      <div class="cliente__colapse__two">
        <ColapseTwo />
        <ColapseTwo />
        <ColapseTwo />
        <ColapseTwo />
        <ColapseTwo />
        <ColapseTwo />
        <ColapseTwo />
      </div>
    </div>
  </div>
</template>
<script>
import Header from "@/components/Header";
import ColapseTwo from "@/components/ColapseTwo";
export default {
  components: {
    Header,
    ColapseTwo,
  },
};
</script>

<style lang="scss" scoped>
.cliente {
  width: 100%;
  height: 100%;
  background: rgb(94, 93, 93);
  &__colapse {
    width: 100%;
    height: auto;
    display: flex;
    justify-content: center;
    &__two {
      width: 1170px;
      height: auto;
      margin-top: 100px;
      display: flex;
      flex-direction: column;
      // justify-content: space-between;
    }
  }
}
</style>
