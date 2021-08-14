<template>
  <main>
    <Menu />
    <Slider />
    <Advantages />
    <About />
  </main>
</template>

<script>
import Menu from '../Menu/Menu.vue'
import Slider from '../Slider/Slider.vue'
import Advantages from '../Advantages/Advantages.vue'
import About from '../About/About.vue'

export default {
  name: 'Main',
  components: {
    Menu,
    Slider,
    Advantages,
    About
  }
}
</script>
