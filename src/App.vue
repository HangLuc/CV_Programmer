<template>
  <div id="app">

    <!--<test></test>
-->
    <!--<router-link to="/components/rou">Rou</router-link>-->
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
  import test from './components/test.vue'
export default {
    components:{
      test
    },
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
