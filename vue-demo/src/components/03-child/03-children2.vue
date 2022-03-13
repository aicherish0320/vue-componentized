<template>
  <div>children2</div>
</template>

<script>
export default {
  name: 'Children2',
  data() {
    return {
      title: 'children2 获取子组件 - title'
    }
  },
  methods: {
    handle() {
      console.log(this.title)
    }
  }
}
</script>

<style scoped></style>
