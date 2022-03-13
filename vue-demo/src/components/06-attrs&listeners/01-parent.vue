<template>
  <div>
    <!-- <myinput
      required
      placeholder="enter your username"
      class="theme-dark"
      data-test="test"
    ></myinput> -->
    <myinput
      required
      placeholder="enter your username"
      class="theme-dark"
      data-test="test"
      @focus="onFocus"
      @input="onInput"
    ></myinput>
    <button @click="handle">按钮</button>
  </div>
</template>

<script>
import myinput from './02-myinput.vue'
export default {
  name: 'Parent',
  components: { myinput },
  methods: {
    onFocus(e) {
      console.log(e)
    },
    onInput(e) {
      console.log(e.target.value)
    },
    handle() {
      console.log(this.value)
    }
  }
}
</script>

<style scoped></style>
