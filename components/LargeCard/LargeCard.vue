<template>
  <NuxtLink :to="`/products/${card.id}`" class="card">
    <img :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)" alt="Fire Extinguisher" class="image">
    <h3 class="header">
      {{ card.title }}
    </h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </NuxtLink>
</template>

<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: ['card']
}
</script>

<style scoped>

a {
  color: black;
}

a:hover {
  text-decoration: none;
}

.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
.snippet {
  color: grey
}
</style>
