<template>
  <main>
    <Menu />
    <Slider />
    <section class="advantages"></section>
    <section class="about"></section>
  </main>
</template>

<script>
import Menu from '../Menu/Menu.vue'
import Slider from '../Slider/Slider.vue'

export default {
  name: 'Main',
  components: {
    Menu,
    Slider
  }
}
</script>

<style>
</style>
