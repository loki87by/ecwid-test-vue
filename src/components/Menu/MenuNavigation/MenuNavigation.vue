<template>
  <ul class="menu__navigation">
    <li v-for="(item, index) in menuItems" :key="index">
      <a href="#" class="menu__item">{{ item }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'MenuNavigation',
  data: function () {
    return {
      menuItems: [
        'Пряжа',
        'Спицы',
        'Крючки',
        'Аксессуары',
        'Подарочные сертификаты',
        'МК и описания',
        'Модели'
      ]
    }
  }
}
</script>

<style>
@import url('../../../blocks/menu/__navigation/menu__navigation.css');
@import url('../../../blocks/menu/__item/menu__item.css');

</style>
