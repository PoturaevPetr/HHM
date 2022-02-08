<template>
  <div id="app">
    <page1/>
    <page2 class="h-100"/>
    <page3/>
  </div>
</template>

<script>
import page1 from './components/page1.vue'
import page2 from './components/page2.vue'
import page3 from './components/page3.vue'

export default {
  name: 'App',
  components: {
    page1,
    page2,
    page3
  }
};
</script>

<style scoped>
page2 {
  background-color: #2d3136;
}
</style>
