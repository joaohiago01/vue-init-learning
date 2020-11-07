<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <User :user="user" :showPassword="true"/>
  </div>
</template>

<script>
import User from './components/User.vue'

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
    User
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
