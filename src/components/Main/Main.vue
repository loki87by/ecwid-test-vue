<template>
  <main>
    <Menu />
    <Slider />
    <Advantages />
    <section class="about"></section>
  </main>
</template>

<script>
import Menu from '../Menu/Menu.vue'
import Slider from '../Slider/Slider.vue'
import Advantages from '../Advantages/Advantages.vue'

export default {
  name: 'Main',
  components: {
    Menu,
    Slider,
    Advantages
  }
}
</script>

<style>
</style>
