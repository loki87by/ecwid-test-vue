<template>
  <ul class='header__info'>
    <li class='header__info-item' v-for="(item, index) in listItems" :key="index">
      <img :alt="item.alt" :src="item.src" />
      <div class="header__info-text">
        <p>{{ item.text1 }}</p>
        <p>{{ item.text2 }}</p>
      </div>
    </li>
  </ul>
</template>

<script>
import position from '../../../../src/assets/icons/position.svg'
import clock from '../../../../src/assets/icons/clock.svg'
import phone from '../../../../src/assets/icons/phone.svg'

export default {
  name: 'HeaderInfo',
  data: function () {
    return {
      listItems: [
        {
          src: position,
          alt: 'adress',
          text1: 'м. Кропоткинская',
          text2: `Соймоновский
    проезд, д.7 с.1`
        },
        {
          src: clock,
          alt: 'work time',
          text1: `Пн - Пт
    11 - 20`,
          text2: `Сб - Вск
    11 - 18`
        },
        {
          src: phone,
          alt: 'adress',
          text1: `+7 800
    000 00 00`,
          text2: `+7 800
    000 00 00`
        }
      ]
    }
  }
}
</script>

<style>
@import url('../../../blocks/header/__info/header__info.css');
@import url('../../../blocks/header/__info-item/header__info-item.css');
@import url('../../../blocks/header/__info-text/header__info-text.css');
</style>
