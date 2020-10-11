<template>
  <div id="app">
    <Dashboard />
  </div>
</template>

<script>
import Dashboard from './components/Dashboard/Dashboard.vue';

export default {
  name: 'App',
  components: {
   Dashboard
  }
}
</script>

<style>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
#app {
padding: 0;
margin: 0;
}
</style>
