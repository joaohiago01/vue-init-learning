<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Client :user="user" />
  </div>
</template>

<script>
import Client from './components/Client.vue'

export default {
  name: 'App',
  data(){
    return {
      user: {
        name: 'Hiago',
        email: 'joaohiago@gmail.com',
        password: '123456'
      }
    }
  },
  components: {
    Client
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
