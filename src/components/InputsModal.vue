<script setup lang="ts">
import ModalInput from "./ModalInput.vue";

// Import Bootstrap's JS
// eslint-disable-next-line @typescript-eslint/no-unused-vars
import { Modal } from "bootstrap";

const inputsConfig = [
  {
    name: "A",
  },
  {
    name: "B",
  },
];
</script>

<template>
  <!-- Modal -->
  <div
    class="modal fade"
    id="inputs-modal"
    tabindex="-1"
    role="dialog"
    aria-labelledby="Inputs Modal"
    aria-hidden="true"
  >
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header justify-content-end">
          <button
            type="button"
            class="close"
            data-bs-dismiss="modal"
            aria-label="Close"
          >
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <template v-for="(input, key) in inputsConfig" :key="key">
            <ModalInput :name="input.name" />
          </template>
        </div>
        <div class="modal-footer">
          <button
            type="button"
            class="btn btn-secondary"
            data-bs-dismiss="modal"
          >
            Close
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
