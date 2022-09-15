<template>
  <div class="home text-center mt-2">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
    <h1>
        Home
    </h1>
    <input type="text" v-model="dataInput">
    <button @click="userClick">User</button>
    <button @click="findClick">Find</button>
  </div>
</template>

<script>
export default {
    data(){
        return {
            dataInput: ""
        }
    },
    methods: {
        userClick(){
            this.$router.push({name: 'user', params: {username: this.dataInput}})
        },
        findClick(){
            this.$router.push({name: 'find', query: {name: this.dataInput}})
        }
    }
}
</script>

<style scoped>
input {
    border: 1px black solid;
}
</style>
