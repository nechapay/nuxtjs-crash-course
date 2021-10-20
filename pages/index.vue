<template>
  <div class="containner">
    <Hero />
    <LargeCardDisplay v-for="cardInfo in largeCardInfo" :key="cardInfo.id" :cardsSection="cardInfo" />
    <SmallCardDisaplay v-for="cardInfo in smallCardInfo" :key="cardInfo.id" :cardsSection="cardInfo" />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'

export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>
