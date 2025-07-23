<template>
  <div class="container mx-auto bg-[#F8FAFC] lg:p-10 p-5">
    <div class="grid lg:grid-cols-3 lg:gap-5 gap-4">
      <div class="space-y-5 bg-white lg:p-5 p-4">
        <h3 class="uppercase font-bold">Доставка до точки клиента (по Москве и МО)</h3>
        <div class="space-y-2.5">
          <p class="font-bold">Условия оформления:</p>
          <ul class="pl-2">
            <li class="relative custom-disc pl-3">
              оформляемся ил кануне дня доставки до 1600 Т
            </li>
          </ul>
        </div>
        <div class="space-y-2.5">
          <p class="font-bold">Стоимость доставки (Москва):</p>
          <DeliveryInfoItem
            :headers="['Сумма чека', 'Стоимость доставки']"
            :rows="[
              { label: 'до 5 000', value: '350 ₽' },
              { label: 'от 5 000', value: '1 ₽', note: 'символическая' },
            ]"
          />
        </div>
        <div class="space-y-2.5">
          <p class="font-bold">За МКАД</p>
          <ul class="pl-2">
            <li class="relative custom-disc pl-3">20 Р вл каждый км о? МКАД.</li>
            <li class="relative custom-disc pl-3">
              При расстоянии более 10 км рассчитывается индивидуально.
            </li>
          </ul>
        </div>
      </div>
      <div class="space-y-5 bg-white lg:p-5 lg:pb-10 p-4">
        <h3 class="uppercase font-bold">Доставка до транспортной компании (по России)</h3>
        <div>
          <p>Мы сотрудничаем с ведущими ТК. доставка возможна в любой регион России</p>
        </div>
        <div class="space-y-2.5">
          <p class="font-bold">Транспортные компании, с которыми мы работаем</p>
          <ul class="pl-2">
            <li class="relative custom-disc pl-3">АЛЕКО</li>
            <li class="relative custom-disc pl-3">БАЙКАЛ-СЕРВИС</li>
            <li class="relative custom-disc pl-3">ВОХСЕККУ</li>
            <li class="relative custom-disc pl-3">ДЕЛОВЫЕ ЛИНИИ</li>
            <li class="relative custom-disc pl-3">МГЙДЖИК ТРАНС</li>
            <li class="relative custom-disc pl-3">ПЭК</li>
            <li class="relative custom-disc pl-3">сдэк</li>
            <li class="relative custom-disc pl-3">ТК «Центр Автомобильных Перевозок*</li>
            <li class="relative custom-disc pl-3">ТК МАГИСТРАЛЬ</li>
            <li class="relative custom-disc pl-3">ТРАНСГАРАНТ</li>
          </ul>
        </div>
        <div class="space-y-5">
          <p class="font-bold">Стоимость доставки до ТК (в пределах МКАД):</p>
          <DeliveryInfoItem
            :headers="['Сумма чека', 'Стоимость доставки']"
            :rows="[
              { label: 'до 5 000', value: '350 ₽' },
              { label: 'от 5 000', value: '1 ₽', note: 'символическая' },
            ]"
          />
        </div>
      </div>
      <div class="space-y-5 bg-white lg:p-5 p-4">
        <h3 class="uppercase font-bold">Самовывоз со склада в москве</h3>
        <div>
          <p>Вы можете забрать товар самостоятельно с нашего склада</p>
        </div>
        <div class="space-y-8">
          <p class="font-bold">Условия самовывом</p>
          <ul class="pl-2">
            <li class="relative custom-disc pl-3">В день оформления заказа.</li>
            <li class="relative custom-disc pl-3">Время отгрузки: с 12:00 до 1800</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import DeliveryInfoItem from "@/components/DeliveryInfoItem.vue";
</script>

<style scoped>
.custom-disc:before {
  position: absolute;
  top: 12px;
  width: 3px;
  height: 3px;
  border-radius: 100%;
  border: 1px solid #000;
  content: "";
  left: 0;
}
</style>
