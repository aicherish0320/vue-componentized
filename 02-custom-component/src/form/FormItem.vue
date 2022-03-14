<template>
  <div>
    <label>{{ label }}</label>
    <div>
      <slot></slot>
      <p v-if="errMessage">{{ errMessage }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AcFormItem',
  props: {
    prop: {
      type: String
    },
    label: {
      type: String
    }
  },
  data() {
    return {
      errMessage: ''
    }
  }
}
</script>

<style scoped></style>
