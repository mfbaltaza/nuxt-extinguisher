<template>
  <div>
    <Hero />
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections } from '@/assets/data'
export default {
  data () {
    return {
      largeCardInfo: largeCardSections
    }
  }
}
</script>
