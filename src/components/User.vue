<template>
    <div>
        <input v-model="user.name"/>
        <br>
        <input type="text" :value="user.email" />
        <br>
        <input type="password" :value="user.password" v-if="showPassword == true"/>
        <p v-else>Hide Password</p>
        <br>
        <button @click="hidePassword">Show Password</button>
        <br>
        <strong>{{user.name}}</strong>
    </div>
</template>

<script>
export default {
    data() {
        return {
            
        }
    },
    props: {
        user: Object,
        showPassword: Boolean
    },
    methods: {
        hidePassword: function() {
            this.showPassword = !this.showPassword;
        }
    }
}
</script>

<style>

</style>