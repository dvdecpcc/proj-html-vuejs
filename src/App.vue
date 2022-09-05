<template>
  <div id="app">
    
  </div>
</template>

<script>
import MyHeader from './components/HelloWorld.vue'
import MyMain from './components/HelloWorld.vue'
import MyFooter from './components/HelloWorld.vue'


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter
  }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.css';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
