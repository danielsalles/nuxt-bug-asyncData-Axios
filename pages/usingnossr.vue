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
mounted: async function() {
  const series = await this.$axios.$get('https://api1.soseriados.net/series?page=1&sort=rating&order=desc&limit=8&nameLIKE=g%')

  this.result = series
}
}
</script>

<style lang="css">
</style>
