<template>
  <div class="container">
    <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const page = await $content("hello").fetch()

    return {
      page,
    }
  },
}
</script>
