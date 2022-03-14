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

      const findParent = (parent) => {
        while (parent) {
          if (parent.$options.name === 'AcFormItem') {
            break
          } else {
            parent = parent.$parent
          }
        }
        return parent
      }

      const parent = findParent(this.$parent)
      if (parent) {
        parent.$emit('validate')
      }
    }
  }
}
</script>

<style scoped></style>
