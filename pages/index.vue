<template>
  <article>
    <h1>{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  name: 'Index',
  layout: 'en',
  async asyncData ({ $content, params }) {
    const page = await $content('/en', 'index').fetch();

    return {
      page
    }
  }
}
</script>
