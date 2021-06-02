<template>
  <div class="modal">
    <div class="modal__center">
      <slot />
    </div>
  </div>
</template>
<script>
export default {};
</script>

<style lang="scss" scoped>
.modal {
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  top: 0;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  &__center {
    width: 40%;
    height: 38%;
    background: #303030;
    border-radius: 4px;
  }
}
</style>
