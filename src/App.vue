<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>{{ car }}</div>
  <abcd msg="My First App"/>
</template>

<script>
import abcd from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    abcd
  },
  data(){
    return {
      car: "Benz"
    }
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
