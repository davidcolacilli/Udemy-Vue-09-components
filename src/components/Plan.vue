<template>
    <div>
        <h3>{{name}}</h3>
        <h4>${{price}}</h4>
    </div>
</template>
<script>
export default {
    name: 'Plan',
    props: {
        name: {
            type: String,
            default: 'Beginner',
            required: true
        },
        price: Number,
    }
}
</script>
<style scoped>
div {background: #f0f0f0; padding: 15px; margin: 15px;}
</style>