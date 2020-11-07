<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div v-for="(user, index) in users" :key="user.id">
      <p>{{index + 1}}</p>
      <User :user="user" showPassword="true"/>
    </div>
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
      },
      users: [
                {
                    id: 1,
                    name: 'João Hiago',
                    email: 'joaohiago@gmail.com',
                    password: '123456'
                },
                {
                    id: 2,
                    name: 'Hiago',
                    email: 'hiago@gmail.com',
                    password: '123456'
                },
                {
                    id: 3,
                    name: 'João',
                    email: 'joao@gmail.com',
                    password: '123456'
                }
            ]
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
