<template>
  <ul class="menu__navigation">
    <li v-for="(item, index) in menuItems" :key="index">
      <a href="#" class="menu__item">{{ item }}</a>
    </li>
  </ul>
</template>

<script>
import { menuItems } from '../../consts/consts'

export default {
  name: 'MenuNavigation',
  data: function () {
    return {
      menuItems: menuItems
    }
  }
}
</script>

<style>
@import url('../../blocks/menu/__navigation/menu__navigation.css');
@import url('../../blocks/menu/__item/menu__item.css');
</style>
