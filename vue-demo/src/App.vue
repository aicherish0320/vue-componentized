<template>
  <div id="app">
    <h1>01-$root</h1>
    <root></root>
    <h1>02-$parent</h1>
    <parent></parent>
    <h1>03-$children</h1>
    <parent1></parent1>
    <h1>04-$ref</h1>
    <parent2></parent2>
    <h1>05-provide&inject</h1>
    <parent3></parent3>
    <h1>06-$attrs&$listeners</h1>
    <parent4></parent4>
  </div>
</template>

<script>
import root from './components/01-root/01-root.vue'
import parent from './components/02-parent/01-parent.vue'
import parent1 from './components/03-child/01-parent.vue'
import parent2 from './components/04-ref/01-parent.vue'
import parent3 from './components/05-provide&inject/01-parent.vue'
import parent4 from './components/06-attrs&listeners/01-parent.vue'

export default {
  name: 'App',
  components: {
    root,
    parent,
    parent1,
    parent2,
    parent3,
    parent4
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
