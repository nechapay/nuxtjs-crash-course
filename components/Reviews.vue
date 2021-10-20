<template>
  <div>
    <h3>Customer Reviews</h3>
    <div>
      <ReviewCard v-for="reviewer in reviewers.results" :key="reviewer.login.uuid" :review="reviewer" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviewers: []
    }
  },
  async fetch() {
    this.reviewers = require('@/assets/users.json')
  }
}
</script>

<style scoped>
</style>