<template>
  <footer>
    <p>
      <span>
        {{ dob }}
      </span>
      <span v-if="dod">
        -
        {{ dod }}
      </span>
    </p>
    <p>
      <small>
        <em>
          Tribute by
          <a :href="authorUrl" target="_blank">
            <strong>
              {{ authorName }}
            </strong>
          </a>
        </em>
      </small>
    </p>
  </footer>
</template>

<script>
export default {
  name: "PageFooter",
  props: {
    authorName: String,
    authorUrl: String,
    dob: String,
    dod: String,
  },
};
</script>

<style scoped lang="sass">
footer
  margin-top: 50px
  width: 100%
  text-align: center
  opacity: 0.5

  p
    margin: 0

  a
    color: white
    text-underline-position: under
</style>
