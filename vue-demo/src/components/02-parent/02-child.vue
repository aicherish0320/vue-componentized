<template>
  <div class="child">
    child
    <br />
    $parent.title: {{ $parent.title }}
    <br />
    <button @click="$parent.handle">获取 $parent.title</button>
    <button @click="$parent.title = 'Hello $parent.title'">
      改变 $parent.title
    </button>

    <grandson></grandson>
  </div>
</template>

<script>
import grandson from './03-grandson.vue'
export default {
  name: 'Child',
  components: { grandson }
}
</script>

<style scoped>
.child {
  border: cyan 2px solid;
}
</style>
