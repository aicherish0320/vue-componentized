<template>
  <div class="grandson">
    grandson
    <br />
    $parent.$parent.title: {{ $parent.$parent.title }}
    <button @click="$parent.$parent.handle">获取 $parent.$parent.title</button>
    <button @click="$parent.$parent.title = 'Hello $parent.$parent.title'">
      改变 $parent.$parent.title
    </button>
  </div>
</template>

<script>
export default {
  name: 'Grandson'
}
</script>

<style scoped>
.grandson {
  border: 2px solid orange;
}
</style>
