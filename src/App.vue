<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Header from './components/Header/Header'
import Main from './components/Main/Main'

export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

<style>
@import url('../normalize.css');
@import url('./assets/fonts/fonts.css');
@import url('./blocks/root/root.css');
</style>
