<template>
    <div>
        <plan v-for="pla in plans" :name="pla.name" :price="pla.price" :key="pla.name"/>
    </div>
</template>

<script>
import Plan from './Plan.vue';
export default {
    name: 'Plans',
    components: {
        Plan
    },
    data() {
        return {
            plans: [
                {
                name: 'Beginner',
                price: 2
                },
                {
                name: 'Intermediate',
                price: 4
                },
                {
                name: 'Advanced',
                price: 6
                },
                {
                name: 'Pro',
                price: 10
                },
            ]
        }
    }
}
</script>

<style scoped>

</style>