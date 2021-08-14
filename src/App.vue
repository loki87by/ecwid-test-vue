<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header/Header'
/* import Main from './components/Main/Main' */

export default {
  name: 'App',
  components: {
    Header
    /* Main */
  }
}
</script>

<style>
header,
.header__info,
.menu__navigation,
.slider__icons,
.advantages,
.advantages__item,
.about {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
}

ul {
  padding: 0;
}

li {
  list-style-type: none;
}

p {
  margin: 0;
}
</style>
