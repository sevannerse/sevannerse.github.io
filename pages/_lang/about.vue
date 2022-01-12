<template>
  <article>
    <h1>{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  name: 'About',
  layout ({ params }) {
    return params.lang
  },
  async asyncData ({ $content, params }) {
    const page = await $content('/' + params.lang, 'about').fetch()

    return {
      page
    }
  }
}
</script>
