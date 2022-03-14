<template>
  <form>
    <slot></slot>
  </form>
</template>

<script>
export default {
  name: 'AcForm',
  provide() {
    return {
      form: this
    }
  },
  props: {
    model: { type: Object },
    rules: { type: Object }
  },
  methods: {
    validate(cb) {
      const tasks = this.$children
        .filter((c) => c.prop)
        .map((c) => c.validate())
      Promise.all(tasks)
        .then(() => {
          cb(true)
        })
        .catch(() => cb(false))
    }
  }
}
</script>

<style scoped></style>
