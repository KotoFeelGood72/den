<template>
  <div class="lg:p-5 p-3 bg-white space-y-2.5">
    <div>
      <img
        :src="product.img.url"
        :alt="product.img.alt"
        class="w-full h-full object-cover"
      />
    </div>
    <ul class="space-y-1">
      <li
        v-for="(item, i) in product.list"
        :key="'product-action-list-item' + i"
        class="flex items-center justify-between gap-2 text-sm"
      >
        <span>{{ item.label }}</span>
        <span :class="[i === product.list.length - 1 ? 'font-bold' : '']">{{
          item.value
        }}</span>
      </li>
    </ul>
    <div class="flex items-center justify-between gap-2">
      <Button name="В КОРЗИНУ" class="max-w-[160px]" />
      <Qty v-model="product.quantity" />
    </div>
    <div class="flex items-center justify-between gap-4 text-sm">
      <p class="opacity-30">Цена с учетом <br />персональной скидки</p>
      <p class="max-w-[78px] text-right text-[#231F20]">В наличии: 334 шт.</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import Button from "./Button.vue";
import Qty from "./Qty.vue";
interface ListItem {
  label: string;
  value: string;
}

interface ProductImage {
  url: string;
  alt: string;
}

interface ProductView {
  img: ProductImage;
  list: ListItem[];
  quantity: number;
}

defineProps<{
  product: ProductView;
}>();
</script>

<style scoped lang="scss"></style>
