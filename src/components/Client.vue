<template>
    <div>
        <input v-model="user.name"/>
        <br>
        <input type="text" :value="user.email">
        <br>
        <input type="password" :value="user.password">
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
        user: Object
    }
}
</script>

<style>

</style>