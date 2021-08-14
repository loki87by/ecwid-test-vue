<template>
  <header>
    <img :src="logo" alt="logo" />
    <HeaderInfo />
    <img :src="basket" alt="basket" />
  </header>
</template>

<script>
import HeaderInfo from '../HeaderInfo/HeaderInfo.vue'
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
@import url('../../blocks/header/header.css');
</style>
