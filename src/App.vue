<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <EmailJS msg="Welcome to My First Email App"/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import EmailJS from './components/EmailJS.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    EmailJS
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
