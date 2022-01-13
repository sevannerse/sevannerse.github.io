<template>
</template>

<script>
export default {
  name: 'Index',
  middleware: [
    function ({ redirect }) {
      redirect('/en')
    },
  ]
}
</script>
