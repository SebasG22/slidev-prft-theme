<script setup lang="ts">
import { computed } from "vue";
const props = defineProps({
  header: {
    type: String,
  },
  text: {
    type: String,
  },
});
</script>

<template>
  <div
    style="
      background-image: url(/figure.svg);
      background-repeat: no-repeat;
      background-position: right;
    "
    class="w-full h-full"
  >
    <div class="my-15 mx-15 w-40">
      <Logo />
    </div>
    <div class="slidev-layout">
      <div class="my-auto">
        <p
          style="color: #b79967"
          class="font-normal tracking-wide uppercase font-serif text-sm"
        >
          {{ props.header }}
        </p>
        <p class="text-4xl">{{ props.text }}</p>
        <slot />
      </div>
    </div>
  </div>
</template>
