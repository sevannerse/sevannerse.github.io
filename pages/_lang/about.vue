<template>
  <div class="mt-5">
  <img src="/profile.jpg" class="w-1/3 rounded-full float-left mr-10 mb-5"></img>
  <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {
  name: 'About',
  layout({ params }) {
    return params.lang
  },
  async asyncData({ $content, params }) {
    const page = await $content('/' + params.lang, 'about').fetch()

    return {
      page,
    }
  },
}
</script>
