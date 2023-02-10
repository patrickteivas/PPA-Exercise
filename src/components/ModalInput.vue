<script setup lang="ts">
import { ref, watch } from "vue";
const props = defineProps({
  name: {
    type: String,
    required: true,
  },
});

const x = ref("");

watch(x, (newX) => {
  console.log(`[${props.name}] ${newX}`);
});
</script>

<template>
  <div class="input-group mb-3">
    <div class="input-group-prepend">
      <span class="input-group-text">{{ props.name }}</span>
    </div>
    <input
      type="text"
      class="form-control"
      :placeholder="props.name"
      :aria-label="props.name"
      v-model="x"
    />
  </div>
</template>
