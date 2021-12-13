<template>
  <div id="app">
    <AppHeader/>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  name: 'App',
  components: {
    AppHeader
  }
}
</script>

<style lang="scss">
*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
</style>
