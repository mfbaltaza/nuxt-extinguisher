<template>
  <div>
    Hello
    {{  product }}
  </div>
</template>

<script>
export default {
  computed: {
    product () {
      return this.$store.getters.getProductId(parseInt(this.$route.params.id))
    }
  }
}
</script>

<style>

</style>
