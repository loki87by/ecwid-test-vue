<template>
  <nav class="menu">
    <MenuNavigation />
  </nav>
</template>

<script>
import MenuNavigation from './MenuNavigation/MenuNavigation.vue'

export default {
  name: 'Menu',
  components: {
    MenuNavigation
  }
}
</script>

<style>
@import url('../../blocks/menu/menu.css');
</style>
