<template>
  <div>
    <myinput ref="mytxt"></myinput>

    <button @click="focus">获取焦点</button>
  </div>
</template>

<script>
import myinput from './02-myinput.vue'
export default {
  name: 'Parent',
  components: { myinput },
  methods: {
    focus() {
      this.$refs.mytxt.focus()
      this.$refs.mytxt.value = 'hello'
    }
  }
}
</script>

<style scoped></style>
