<template>
  <div class="space-y-2.5 bg-white py-2.5 px-5 w-full">
    <h6 class="font-bold">{{ block.title }}</h6>
    <ul class="text-sm space-y-1">
      <li
        v-for="(item, i) in block.list"
        :key="'block-list-item-' + i"
        class="flex gap-3 justify-between items-center"
      >
        <span>{{ item.label }}</span>
        <span>{{ item.value }}</span>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
interface ListTextItem {
  label: string;
  value: string;
}

interface Blocktext {
  title: string;
  list: ListTextItem[];
}

defineProps<{
  block: Blocktext;
}>();
</script>

<style scoped lang="scss"></style>
