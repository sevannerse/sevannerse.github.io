<template>
  <article>
    <h1>{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  name: 'Post',
  layout ({ params }) {
    return params.lang
  },
  async asyncData ({ $content, params }) {
    const page = await $content('/' + params.lang + '/posts', params.slug).fetch()

    return {
      page
    }
  }
}
</script>
