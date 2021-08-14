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
import { listItems } from '../../consts/consts'

export default {
  name: 'HeaderInfo',
  data: function () {
    return {
      listItems: listItems
    }
  }
}
</script>

<style>
@import url('../../blocks/header/__info/header__info.css');
@import url('../../blocks/header/__info-item/header__info-item.css');
@import url('../../blocks/header/__info-text/header__info-text.css');
</style>
