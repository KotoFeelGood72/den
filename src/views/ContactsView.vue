<template>
  <section id="contacts" class="bg-[#F8FAFC]">
    <div class="max-w-[1078px] container mx-auto lg:space-y-[30px]">
      <div
        id="contacts-top"
        class="bg-white flex flex-wrap item-start lg:gap-[77px] lg:p-5 p-4 gap-5 lg:text-base text-sm"
      >
        <div>
          <p>Ведущий менеджер</p>
          <p>Специалист отдела обработки</p>
        </div>
        <div>
          <ul
            class="flex items-start max-lg:justify-between lg:gap-[75px] lg:text-base text-sm"
          >
            <li class="font-bold">
              <p>Иван Васин</p>
              <p>Тарас Петров</p>
            </li>
            <li>
              <p>+7 (916) 123-45-67</p>
              <p>+7 (916) 123-45-67</p>
            </li>
            <li>
              <p>ivan.v@gmail.com</p>
              <p>ivan.v@gmail.com</p>
            </li>
          </ul>
        </div>
      </div>
      <div class="lg:p-5 p-4 bg-white lg:space-y-[47px] space-y-5">
        <h3 class="lg:text-[28px] font-bold uppercase">Контакты</h3>
        <div class="lg:gap-[37px] flex flex-wrap gap-5">
          <div class="lg:max-w-[258px] text-sm">
            <p class="font-bold">ООО "ДЕНКИРС РУС"</p>
            <p>ОГРН 1187746605639</p>
            <p>ИНН 9731004945</p>
            <p>Офис - Москва, Большая Очаковская ул. ,47А, стр. 1, офис 211</p>
            <p>Склад - Москва, ул. Василия <br />Петушкова, д. 3, к 1</p>
            <p class="font-bold">Время работы:</p>
            <p>ПН-ПТ: с 09:00 до 18:00 <br />СБ-ВС: выходной</p>
            <p class="font-bold">Оптовый отдел:</p>
            <p>+7 (495) 859-27-05, доб. <br />1opt@denkirs.ru</p>
            <p class="font-bold">Розничный отдел:</p>
            <p>+7 (495) 859-27-05, доб. 2</p>
            <p>Проектный отдел:</p>
            <p>+7 (495) 859-27-05, доб. 3 <br />project@denkirs.ru</p>
            <p class="font-bold">Гарантия и рекламации:</p>
            <p>+7 (495) 159-48-37, доб. <br />4 warranty@denkirs.ru</p>
            <p class="font-bold">HR-отдел:</p>
            <p>+7 (925) 248-49-35 <br />hr@denkirs.ru</p>
          </div>
          <div class="w-full lg:h-[469px] h-[300px] max-w-[743px] relative">
            <div class="absolute inset-0 z-10 pointer-events-none w-full h-full">
              <div class="w-full h-full backdrop-grayscale"></div>
            </div>
            <iframe
              src="https://yandex.ru/map-widget/v1/?um=constructor%3A26053256f8f24a300c2c73adf582c837f3af907c068a6daa0048eeb2286c54e5&amp;source=constructor"
              width="100%"
              height="100%"
              frameborder="0"
            ></iframe>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { onMounted } from "vue";
</script>
