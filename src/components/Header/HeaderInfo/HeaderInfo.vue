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
  name: 'Header',
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
.header__info {
  width: 753px;
  margin: 0;
  margin-left: -26px;
}

.header__info-item {
  width: -webkit-max-content;
  width: -moz-max-content;
  width: max-content;
  height: -webkit-max-content;
  height: -moz-max-content;
  height: max-content;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}

.header__info-item:first-of-type {
  margin-left: 5px;
}

.header__info-item:nth-of-type(2) {
  margin-right: 18px;
}

.header__info-item:nth-of-type(3) {
  margin-right: -17px;
}

.header__info-text {
  margin-left: 17px;
  font-family: "Bw Modelica Cyrillic DEMO", sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 13px;
  line-height: 16px;
  color: #535353;
}

@media (max-width: 1000px) {
  .header__info {
    width: 70%;
  }

  .header__info-item:first-of-type {
    margin: 0;
  }

  .header__info-item:nth-of-type(2) {
    margin: 0;
  }

  .header__info-item:nth-of-type(3) {
    margin: 0;
  }
}

@media (max-width: 888px) {
  .header__info-text {
    margin-left: 5px;
  }
}

@media (max-width: 800px) {
  .header__info-text {
    white-space: pre;
    text-align: end;
    line-height: 1;
  }
}

@media (max-width: 710px) {
  .header__info-text {
    font-size: 10px;
  }
}

@media (max-width: 555px) {
  .header__info-text {
    font-size: 8px;
  }
}

@media (max-width: 500px) {
  .header__info-item > img {
    width: 20%;
  }
}

</style>
