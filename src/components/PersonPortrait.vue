<template>
  <article>
    <header>
      <h1>
        {{ title }}
      </h1>
      <img class="portrait" :src="image" />
      <img class="cloud" src="../assets/cloud.png" />
    </header>
    <div class="body">
      <p>
        {{ description }}
      </p>
    </div>
  </article>
</template>

<script>
export default {
  name: "PersonPortrait",
  props: {
    title: String,
    description: String,
    image: String,
  },
}
</script>

<style scoped lang="sass">
header
  position: relative
  height: 300px

  h1, img
    position: absolute

  h1
    z-index: 1
    text-transform: uppercase
    letter-spacing: 0.1em
    font-weight: 550
    font-size: 2.2rem
    line-height: 1.2
    margin: 0
    bottom: 25px
    text-shadow: 2px 2px 0.5rem #000
    animation-name: float-5, fw
    animation-duration: 10s, 10s
    animation-delay: 0.5s, 0s
    animation-timing-function: ease-in-out, ease-in-out
    animation-iteration-count: infinite, infinite
    color: #fffe

  .portrait
    width: 200px
    animation-name: float-5, bs
    animation-duration: 10s, 10s
    animation-delay: 1.5s, 0s
    animation-timing-function: ease-in-out, ease-in-out
    animation-iteration-count: infinite, infinite
    box-shadow: 0px 0px 100px 10px #fff6
    border-top-right-radius: 100px
    border-bottom-left-radius: 50px
    right: 0%

    @media (min-width: 768px)
      right: -15%

  .cloud
    width: 400px
    left: -40%
    bottom: -40px
    transform: translatey(0px)
    animation: float 10s ease-in-out infinite
    animation-delay: 0.5s
    opacity: 0.67

    @media (min-width: 768px)
      opacity: 0.5

.body
  line-height: 1.5
  letter-spacing: 0.1em
  text-align: right
  font-weight: 300
</style>
