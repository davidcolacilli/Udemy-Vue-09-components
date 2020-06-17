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
h1 {
	text-align: center;
	margin-bottom: 3rem;
	font: normal 3.5rem 'Eater', cursive;
	color: #B3BD5E;
}
</style>