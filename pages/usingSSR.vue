<template>
  <div class="">
    result: {{ result }}
  </div>
</template>

<script>
export default {
  data () {
  return { result: '' }
},
async asyncData ({ $axios }) {
  const series = await $axios.$get('https://api1.soseriados.net/series?page=1&sort=rating&order=desc&limit=8&nameLIKE=g%')
  return { result: series }
}
}
</script>

<style lang="css">
</style>
