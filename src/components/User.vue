<template>
    <div>
        <input v-model="user.name"/>
        <br>
        <input type="text" :value="user.email" />
        <br>
        <input type="password" :value="user.password" v-if="showPassword == false"/>
        <p v-else>Hide Password</p>
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
    }
}
</script>

<style>

</style>