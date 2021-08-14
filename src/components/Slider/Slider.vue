<template>
  <section class="slider">
    <div class="slider__wrapper">
      <img
        v-for="(slide, index) in slides"
        :key="index"
        :alt="slide.alt"
        :src="slide.src"
        class="slider__image"
      />
    </div>
    <button
      type="button"
      class="slider__button slider__button_position_left"
      @click="toLeft"
    ></button>
    <div class="slider__icons">
      <div class="slider__icon slider__icon_active"
      @click="toSlide"></div>
      <div class="slider__icon"
      @click="toSlide"></div>
      <div class="slider__icon"
      @click="toSlide"></div>
      <div class="slider__icon"
      @click="toSlide"></div>
      <div class="slider__icon"
      @click="toSlide"></div>
    </div>
    <button
      type="button"
      class="slider__button slider__button_position_right"
      @click="toRight"
    ></button>
  </section>
</template>

<script>
import { slides } from '../../consts/consts'
import { changeSlide, clickSlide } from '../../consts/helpers.js'

export default {
  name: 'Slider',
  data: function () {
    return {
      slides: slides
    }
  },
  methods: {
    init: function () {
      const slider = document.querySelector('.slider__wrapper')
      const icons = document.querySelector('.slider__icons')
      const firstCopy = slider.children[0].cloneNode(true)
      const lastCopy = slider.children[slider.children.length - 1].cloneNode(
        true
      )
      slider.appendChild(firstCopy)
      slider.insertBefore(lastCopy, slider.children[0])

      for (let i = 0; i < slider.children.length; i++) {
        slider.children[i].style = 'transform: translateX(-100%)'
      }

      icons.children[0].classList.add('slider__icon_active')
    },
    toLeft: function () {
      changeSlide(0, this.sliderData)
    },
    toRight: function () {
      changeSlide(1, this.sliderData)
    },
    toSlide: function (event) {
      clickSlide(event, this.sliderData)
    }
  },
  mounted () {
    this.init()
    const slider = document.querySelector('.slider__wrapper')
    const icons = document.querySelector('.slider__icons')
    let slidePosition = 1
    this.sliderData = {
      slides: slider.children,
      pos: slidePosition,
      icons: icons.children,
      activeIconClass: 'slider__icon_active',
      shift: 100,
      shiftUnit: '%',
      limit: 1
    }
  }
}
</script>

<style>
@import url("../../blocks/slider/slider.css");
@import url("../../blocks/slider/__wrapper/slider__wrapper.css");
@import url("../../blocks/slider/__image/slider__image.css");
@import url("../../blocks/slider/__button/slider__button.css");
@import url("../../blocks/slider/__button/_position/slider__button_position_left.css");
@import url("../../blocks/slider/__button/_position/slider__button_position_right.css");
@import url("../../blocks/slider/__icons/slider__icons.css");
@import url("../../blocks/slider/__icon/slider__icon.css");
@import url("../../blocks/slider/__icon/_active/slider__icon_active.css");
</style>
