<template>
  <div :class="{ modal: true, 'fade-in': isOpenModal }">
    <h2 class="modal-title">{{ title }}</h2>
    <p class="modal-text">{{ message }}</p>
    <section class="modal-actions">
      <button class="modal-actions-button">{{ textButton }}</button>
    </section>
  </div>
  <div :class="{ 'modal-opacity': true, active: isOpenModal }"></div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "PxModal",
  props: {
    title: String,
    message: String,
    textButton: String,
    isOpenModal: Boolean,
  },
  setup() {},
};
</script>

<style lang="scss" scoped>
@import "~@/assets/sass/6-Components/Modal/_modal.scss";
</style>
