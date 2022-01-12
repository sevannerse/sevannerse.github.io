<template>
  <article>
    <h1>{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  name: 'Index',
  layout ({ params }) {
    return params.lang || 'en';
  },
  async asyncData ({ $content, params }) {
    const page = await $content('/' + (params.lang || 'en'), 'index').fetch();

    return {
      page
    }
  }
}
</script>
