<template>
  <div class="container">
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo.slice(0, 1)"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCardInfo"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data'
export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>

<style scoped>
</style>
