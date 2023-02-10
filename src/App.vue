<script setup lang="ts">
import InputsModal from "./components/InputsModal.vue";

import { ref } from "vue";

const isModalOpen = ref(false);

const toggleModal = (forceValue?: boolean) => {
  isModalOpen.value = forceValue ?? !isModalOpen.value;
};
</script>

<template>
  <button
    type="button"
    class="btn btn-dark"
    title="Open modal"
    data-bs-toggle="modal"
    data-bs-target="#inputs-modal"
  >
    Nupp 1
  </button>

  <InputsModal :show-modal="isModalOpen" @modalClosed="toggleModal(false)" />
</template>
