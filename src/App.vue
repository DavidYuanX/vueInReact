<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <my-react-component :message="message" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import { ReactInVue } from 'vuera'
import reactTest from './react_test'

export default {
  name: 'App',
  data () {
    return {
      message: 'Hello from React!'
    }
  },
  components: { 'my-react-component': ReactInVue(reactTest), HelloWorld }
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
