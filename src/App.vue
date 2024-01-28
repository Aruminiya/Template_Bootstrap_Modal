<script>
import Modal from "./components/Modal.vue";

export default {
  components: { Modal },
  methods: {
    modalClick() {
      // Vue 可以透過 $refs 在父組件操作 子組件的方法或狀態
      this.$refs.modalTemplate.modalShow();
    },
  },
};
</script>

<template>
  <div>
    <h1>按下按鈕打開 Modal</h1>
    <button type="button" class="btn btn-primary" @click="modalClick()">
      打開 Modal
    </button>
    <Modal ref="modalTemplate" />
  </div>
</template>

<style lang="scss" scoped></style>
