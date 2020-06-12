<template>
    <h1>{{heading}}</h1>
</template>

<script>
export default {
    name: 'HeaderComponent',
    props: {
        heading: String
    }
}
</script>

<style scoped>
h1 {text-align: center;}
</style>