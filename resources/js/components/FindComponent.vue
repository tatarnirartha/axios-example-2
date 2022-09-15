<template>
    <div class="text-center">
        <h1>Find {{this.$route.query.name}} Query</h1>
        <button @click="goBack">Back</button>
        <button @click="goHome">Go Home</button>
    </div>
</template>

<script>
export default {
    methods: {
        goBack(){
            this.$router.go({name: 'home'})
        },
        goHome(){
            this.$router.push({name: 'home'})
        }
    }
}
</script>