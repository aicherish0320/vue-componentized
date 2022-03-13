<template>
  <div class="parent">
    parent
    <child></child>
  </div>
</template>

<script>
import child from './02-child.vue'
export default {
  name: 'Parent',
  components: { child },
  data() {
    return {
      title: '获取父组件实例'
    }
  },
  methods: {
    handle() {
      console.log(this.title)
    }
  }
}
</script>

<style scoped>
.parent {
  border: 2px solid red;
}
</style>
