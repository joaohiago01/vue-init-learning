<template>
    <div>
        <input v-model="user.name"/>
        <br>
        <input type="text" :value="user.email" />
        <br>
        <input type="text" :value="user.password" v-if="showPassword == true"/>
        <p v-else>Hide Password</p>
        <br>
        <button @click="hidePassword">{{passwordShowText}} Password</button>
        <br>
        <br>
        <strong>{{user.name | capsLockText}}</strong>
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
        showPassword: Boolean,
        passwordShowText: String
    },
    methods: {
        hidePassword: function() {
            this.showPassword = !this.showPassword;
            if (!this.showPassword) {
                this.passwordShowText = 'Show'
            } else {
                this.passwordShowText = 'Hide'
            }
        }
    },
    filters: {
        capsLockText: function(value) {
            return value.toUpperCase();
        }
    }
}
</script>

<style>

</style>