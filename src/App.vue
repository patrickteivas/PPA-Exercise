<script setup lang="ts">
import InputsModal from "./components/InputsModal.vue";
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

  <InputsModal />
</template>
