<template>
  <div>
    <PersonPortrait :title="title" :description="description" :image="image" />
    <PageFooter
      :author-name="authorName"
      :author-url="authorUrl"
      :dob="dob"
      :dod="dod"
    />
  </div>
</template>

<script setup>
import PersonPortrait from "./components/PersonPortrait.vue"
import PageFooter from "./components/PageFooter.vue"
import { ref } from "vue"

/**
 * Specify the name of the person you want to tribute.
 */
const title = ref("Valentina Caesar")

/**
 * Specify the description of the person you want to tribute.
 */
const description = ref(
  "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras luctus nulla nec eleifend dignissim. Vestibulum varius semper turpis et lacinia. Quisque feugiat pellentesque mauris, at convallis quam elementum laoreet."
)

/**
 * Specify the image of the person you want to tribute.
 *
 * @see https://stackoverflow.com/a/69896214/13765033
 */
const image = ref(require("./assets/portrait-female-2.jpeg"))

/**
 * Specify the date of birth of the person you want to tribute.
 */
const dob = ref("1867")

/**
 * Specify the date of death of the person you want to tribute.
 */
const dod = ref("1931")

/**
 * Specify the name of the person you want to credit (your name).
 */
const authorName = ref("devidw")

/**
 * Specify the URL of the person you want to credit (your website).
 */
const authorUrl = ref("https://github.com/devidw")
</script>

<style lang="sass">
@import ./css/app

body
  min-height: 100vh
  background-color: black
  background-image: url(./assets/stars.webp)
  // background-size: cover
  background-size: 100% 100%
  background-repeat: no-repeat
  background-position: center
  color: white
  font-family: 'mono'
  hyphens: auto
  display: flex
  align-items: center
  animation-name: bg
  animation-delay: 0.5s
  animation-duration: 30s
  animation-iteration-count: infinite
  animation-timing-function: ease-in-out

#app
  margin-left: auto
  margin-right: auto
  max-width: 320px

  @media (min-width: 768px)
    max-width: 340px
</style>
