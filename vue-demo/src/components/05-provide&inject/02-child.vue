<template>
  <div class="child">
    child
    <br />
    title: {{ title }}
    <br />
    <button @click="handle">获取 title</button>
    <button @click="title = 'xxx'">改变 title</button>

    <grandson></grandson>
  </div>
</template>

<script>
import grandson from './03-grandson.vue'
export default {
  name: 'Child',
  components: { grandson },
  inject: ['title', 'handle']
}
</script>

<style scoped>
.child {
  border: 2px solid red;
}
</style>
