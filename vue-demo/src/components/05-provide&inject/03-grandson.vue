<template>
  <div class="grandson">
    grandson
    <br />
    title: {{ title }}
    <br />
    <button @click="handle">获取 title</button>
    <button @click="title = 'yyy'">改变 title</button>
  </div>
</template>

<script>
export default {
  name: 'Grandson',
  inject: ['title', 'handle']
}
</script>

<style scoped>
.grandson {
  border: 2px solid cyan;
}
</style>
