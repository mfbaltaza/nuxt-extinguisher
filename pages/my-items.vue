<template>
  <div class="container">
    <h1>Let's go on a renting spree</h1>
    <NuxtLink to="/">
      Go Home
    </NuxtLink>
    <MyItem
      v-for="item in myRentals"
      :key="item.id"
      :item="item"
    />
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: {
    ...mapState(['myRentals'])
  }
}
</script>

<style scoped>
h1 {
    font-size: 1.75rem;
    margin-top: 1rem;
}
h6 {
    font-size: 1.15rem;
    font-weight: 400;
}
p {
    color: grey
}

</style>
