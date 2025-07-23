<template>
  <section id="product" class="bg-[#F8FAFC]">
    <div class="container space-y-3 mx-auto max-lg:p-5">
      <h1 class="lg:text-base font-bold">Накладной светильник Denkirs DK2003-BK</h1>

      <div class="flex lg:gap-5 flex-wrap">
        <div class="max-lg:flex-grow">
          <ProductViewAction :product="ProductView" />
        </div>
        <div class="space-y-5 flex-grow max-w-4xl">
          <BlockDescription :block="blockDescription" />
          <div
            class="columns-1 lg:columns-2 lg:space-x-5 lg:space-y-5 space-y-3 space-x-3 w-full"
          >
            <ListTextCol
              :block="item"
              v-for="(item, i) in blockList"
              :key="'list-block-item-' + i"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import BlockDescription from "@/components/BlockDescription.vue";
import ListTextCol from "@/components/ListTextCol.vue";
import ProductViewAction from "@/components/ProductViewAction.vue";
import { ref } from "vue";

const blockDescription = {
  title: "Описание",
  description:
    "Deep - серия встраиваемых влагозащищенных светильников из полимера под сменную лампу. Тонкая внешняя рамка подчеркивает минималистичный дизайн. Матовый рассеиватель большого диаметра хорошо рассеивает свет, а его размещение в углублении корпуса светильника снижает слепящий эффект. Серия идеально подходит для влажных помещений. Лампа в комплект не входит. Для данной серии рекомендуем ультратонкие модули SLIM LED в качестве источника света, монтажная глубина всего 50 мм.",
};

const blockList = [
  {
    title: "Основные характеристики",
    list: [
      { label: "материал арматуры", value: "алюминий" },
      { label: "материал плафона", value: "алюминий" },
      { label: "цвет арматуры", value: "белый" },
      { label: "цвет плафона", value: "белый" },
      { label: "форма", value: "круг" },
      { label: "форма плафона", value: "Цилиндр" },
      { label: "тип светильника", value: "подвесной" },
      { label: "серия", value: "Denkirs Solid" },
      { label: "коллекция", value: "SOLID Tube" },
      { label: "гарантия", value: "3 года" },
      { label: "страна происхождения", value: "Словения" },
      { label: "тип монтажа", value: "встраиваемый" },
      { label: "подходит для натяжных потолков", value: "да/нет" },
      { label: "ОСОБЕННОСТИ", value: "Низкая лампа каления" },
    ],
  },
  {
    title: "Управление и функции",
    list: [
      { label: "выключатель", value: "Нет" },
      { label: "пульт управления", value: "ДА" },
      {
        label: "управляется голосовыми помощниками",
        value: "Алиса, Маруся, Салют, Google assistant, Siri",
      },
      { label: "управляется приложениями", value: "Smart Life" },
      { label: "управляется экосистемами", value: "Tuya" },
      { label: "тип управления", value: "голосовое управление" },
    ],
  },
  {
    title: "Электротехнические параметры",
    list: [
      { label: "тип цоколя", value: "GU10" },
      { label: "мощность лампы", value: "15" },
      { label: "мощность общая", value: "15" },
      { label: "количество ламп", value: "1" },
      { label: "цвет свечения", value: "" },
      { label: "световой поток", value: "" },
      { label: "лампы в комплекте", value: "Нет" },
      { label: "степень защиты ip", value: "20" },
      { label: "напряжение", value: "220" },
      { label: "диммируется", value: "" },
      { label: "угол рассеивания света", value: "" },
    ],
  },
  {
    title: "Размеры",
    list: [
      { label: "высота", value: "1800" },
      { label: "длина цепи", value: "1500" },
      { label: "высота минимальная", value: "400" },
      { label: "длина", value: "52" },
      { label: "ширина/диаметр", value: "52" },
      { label: "монтажное отверстие (диаметр)", value: "" },
      { label: "количество грузовых мест", value: "1" },
      { label: "вес коробки", value: "0.65" },
      { label: "размер коробки (ДхШхВ)", value: "410х100х85" },
      { label: "объем коробки", value: "0.003" },
    ],
  },
];

const ProductView = ref<any>({
  img: {
    url: "product.jpg",
    alt: "Карточка товара",
  },
  list: [
    { label: "Код товара:", value: "0000000" },
    { label: "Артикул:", value: "DK0000-BK" },
    { label: "Цена:", value: "4 990 Р" },
  ],
  quantity: 0,
});
</script>

<style scoped lang="scss"></style>
