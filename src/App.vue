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
import PersonPortrait from "./components/PersonPortrait.vue";
import PageFooter from "./components/PageFooter.vue";
import { ref } from "vue";

const title = ref("Valentina Caesar");
const description = ref(
  "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras luctus nulla nec eleifend dignissim. Vestibulum varius semper turpis et lacinia. Quisque feugiat pellentesque mauris, at convallis quam elementum laoreet."
);
// const image = ref("./assets/portrait.png");
const authorName = ref("devidw");
const authorUrl = ref("https://github.com/devidw");
const dob = ref("1867");
const dod = ref("1931");
</script>

<style lang="sass">
@import ./css/app

body
  min-height: 100vh
  background-color: black
  background-image: url(./assets/stars.webp)
  background-size: cover
  // background-size: 100% 100%
  background-repeat: no-repeat
  background-position: center
  color: white
  font-family: 'mono'
  hyphens: auto
  display: flex
  align-items: center
  // animation-name: bg
  // animation-delay: 0.5s
  // animation-duration: 30s
  // animation-iteration-count: infinite
  // animation-timing-function: ease-in-out

#app
  margin-left: auto
  margin-right: auto
  max-width: 320px

  @media (min-width: 768px)
    max-width: 340px
</style>
