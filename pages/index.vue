<template>
  <div class="containner">
    <Nav />
    <Hero />
    <LargeCardDisplay v-for="cardInfo in largeCardInfo" :key="cardInfo.id" :cardsSection="cardInfo" />
    <SmallCardDisaplay v-for="cardInfo in smallCardInfo" :key="cardInfo.id" :cardsSection="cardInfo" />
  </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import LargeCardDisplay from '~/components/LargeCardDisplay.vue'
import { largeCardSections, smallCardSections } from '@/assets/data.js'
import SmallCardDisaplay from '~/components/SmallCardDisaplay.vue'
import Nav from '~/components/Nav.vue'

export default {
  components: { Hero, LargeCardDisplay, SmallCardDisaplay, Nav },
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>
