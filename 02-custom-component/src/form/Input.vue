<template>
  <div>
    <input :type="type" :value="value" @input="handleInput" v-bind="$attrs" />
  </div>
</template>

<script>
export default {
  name: 'AcInput',
  inheritAttrs: false,
  props: {
    value: {
      type: String
    },
    type: {
      type: String,
      default: 'text'
    }
  },
  methods: {
    handleInput(e) {
      this.$emit('input', e.target.value)
    }
  }
}
</script>

<style scoped></style>
