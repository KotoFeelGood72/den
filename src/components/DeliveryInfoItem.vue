<template>
  <div class="max-w-md lg:text-base text-black">
    <div class="flex justify-between gap-4">
      <span v-for="(item, i) in headers" :key="'headers-item-delivery-' + i">{{
        item
      }}</span>
    </div>
    <ul class="space-y-0.5">
      <li v-for="(row, index) in rows" :key="index" class="flex items-end">
        <span class="whitespace-nowrap">{{ row.label }}</span>
        <div class="flex-1 mx-2 border-b border-dotted border-black h-0 mb-1.5"></div>
        <span class="whitespace-nowrap">
          {{ row.value }}
          <span v-if="row.note">({{ row.note }})</span>
        </span>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  headers?: [string, string];
  rows: {
    label: string;
    value: string;
    note?: string;
  }[];
}>();
</script>

<style scoped></style>
