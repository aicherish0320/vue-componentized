<template>
  <form>
    <slot></slot>
  </form>
</template>

<script>
export default {
  name: 'AcForm',
  props: {
    model: { type: Object },
    rules: { type: Object }
  }
}
</script>

<style scoped></style>
