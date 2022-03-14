<template>
  <div>
    <steps :count="count" :active="active"></steps>
    <button @click="next">下一步</button>
  </div>
</template>

<script>
import Steps from './Steps.vue'
export default {
  name: 'StepsTest',
  components: {
    Steps
  },
  data() {
    return {
      count: 5,
      active: 0
    }
  },
  methods: {
    next() {
      this.active++
    }
  }
}
</script>

<style scoped></style>
