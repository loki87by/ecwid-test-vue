<template>
  <section class="advantages">
    <div class="advantages__item" v-for="(advantage, index) in advantages" :key="index" >
      <img :alt="advantage.alt" :src="advantage.src" />
      <h3 class="advantages__text">
        <span>{{ advantage.text1 }}</span>
        <span>{{ advantage.text2 }}</span>
      </h3>
    </div>
  </section>
</template>

<script>
import sheep from '../../../src/assets/icons/sheep.svg'
import star from '../../../src/assets/icons/star.svg'
import car from '../../../src/assets/icons/car.svg'
import geoposition from '../../../src/assets/icons/geoposition.svg'
import operator from '../../../src/assets/icons/operator.svg'

export default {
  name: 'Advantages',
  data: function () {
    return {
      advantages: [{
        src: sheep,
        alt: 'Natural',
        text1: 'Только',
        text2: 'натуральный состав'
      },
      {
        src: star,
        alt: 'Actual',
        text1: 'Актуальное',
        text2: 'наличие на сайте'
      },
      {
        src: car,
        alt: 'Quickly',
        text1: 'Быстрая',
        text2: 'отправка'
      },
      {
        src: geoposition,
        alt: 'Convenience',
        text1: 'Удобное',
        text2: 'расположение'
      },
      {
        src: operator,
        alt: 'Help',
        text1: 'Помощь',
        text2: 'в подборе товаров'
      }]
    }
  }
}
</script>

<style>
@import url('../../blocks/advantages/advantages.css');
@import url('../../blocks/advantages/__item/advantages__item.css');
@import url('../../blocks/advantages/__text/advantages__text.css');
</style>
