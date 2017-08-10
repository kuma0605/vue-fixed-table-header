<template>
  <div id="app">
    <fixed-header-table></fixed-header-table>
  </div>
</template>

<script>
import fixed_header_table from "./fixed-table-header.vue";
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    "fixed-header-table":fixed_header_table
  }
}
</script>

<style lang="scss">

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  // color: #2c3e50;
  margin-top: 60px;
}

</style>
