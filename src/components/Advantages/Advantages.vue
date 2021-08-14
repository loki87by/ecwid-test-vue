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
import { advantages } from '../../consts/consts.js'

export default {
  name: 'Advantages',
  data: function () {
    return {
      advantages: advantages
    }
  }
}
</script>

<style>
@import url('../../blocks/advantages/advantages.css');
@import url('../../blocks/advantages/__item/advantages__item.css');
@import url('../../blocks/advantages/__text/advantages__text.css');
</style>
