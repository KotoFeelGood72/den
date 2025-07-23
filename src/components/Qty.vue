<template>
  <div class="flex border divide-x divide-black">
    <button
      type="button"
      class="w-10 h-10 flex items-center justify-center bg-[#F8FAFC] leading-0 cursor-pointer"
      @click="decrement"
    >
      −
    </button>
    <div class="w-10 h-10 flex items-center justify-center lg:text-base">
      {{ modelValue }}
    </div>
    <button
      type="button"
      class="w-10 h-10 flex items-center justify-center bg-[#F8FAFC] leading-0 cursor-pointer"
      @click="increment"
    >
      +
    </button>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  modelValue: number;
}>();

const emit = defineEmits<{
  (e: "update:modelValue", value: number): void;
}>();

const increment = () => {
  emit("update:modelValue", props.modelValue + 1);
};

const decrement = () => {
  if (props.modelValue > 1) {
    emit("update:modelValue", props.modelValue - 1);
  }
};
</script>

<style scoped></style>
