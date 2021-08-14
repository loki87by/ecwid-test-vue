<template>
  <header>
    <img :src="logo" alt="logo" />
    <HeaderInfo />
    <img :src="basket" alt="basket" />
  </header>
</template>

<script>
import HeaderInfo from './HeaderInfo/HeaderInfo.vue'
import logoHeader from '../../../src/assets/icons/logo_header.svg'
import basket from '../../../src/assets/icons/basket.svg'

export default {
  name: 'Header',
  components: {
    HeaderInfo
  },
  data: function () {
    return {
      logo: logoHeader,
      basket: basket
    }
  }
}
</script>

<style>
header {
  width: 1098px;
  padding: 30px 57px 19px 45px;
  margin: auto;
}

@media (max-width: 1199px) {
  header {
    width: calc(100% - 102px);
  }
}

@media (max-width: 1036px) {
  header {
    width: calc(100% - 60px);
    padding: 20px 30px;
  }
}

@media (max-width: 710px) {
  header {
    width: calc(100% - 30px);
    padding: 10px 15px;
  }
}

@media (max-width: 500px) {
  header > img {
    max-width: 10%;
  }
}
</style>
