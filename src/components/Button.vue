<template>
  <button
    type="button"
    class="bg-black py-3 px-4 text-white transition-all hover:bg-white hover:text-black cursor-pointer border border-black w-full leading-none max-h-[41px]"
  >
    {{ name }}
  </button>
</template>

<script setup lang="ts">
defineProps<{
  name: string;
}>();
</script>

<style scoped lang="scss"></style>
