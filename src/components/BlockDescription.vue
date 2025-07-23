<template>
  <div class="lg:py-6 lg:px-5 px-4 py-4 bg-white space-y-2.5">
    <h3 class="font-bold lg:text-base">{{ block.title }}</h3>
    <div class="text-sm">{{ block.description }}</div>
  </div>
</template>

<script setup lang="ts">
interface BlockText {
  title: string;
  description: string;
}
defineProps<{
  block: BlockText;
}>();
</script>

<style scoped lang="scss"></style>
