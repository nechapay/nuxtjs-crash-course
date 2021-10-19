<template>
  <div>
    <Nav />
    <div class="container">      
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0, 1)"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisaplay 
        v-for="cardInfo in smallCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import LargeCardDisplay from "~/components/LargeCardDisplay.vue"
import { largeCardSections, smallCardSections } from "@/assets/data.js"
import Nav from "~/components/Nav.vue"
import SmallCardDisaplay from "~/components/SmallCardDisaplay.vue"
export default {
  components: { LargeCardDisplay, Nav, SmallCardDisaplay},
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>

<style scoped>
</style>