<template>
    <div>
        <div class="container">
            <plan v-for="(pla) in plans" 
                :name="pla.name" 
                :price="pla.price" 
                :isSelected="isPlanSelected(pla)" 
                :key="pla.name" 
                @toggleSelect="togglePlanSelected"/>
        </div>
        <div v-if="planSelected" 
            class="summary">
            <strong>Selected plan: </strong> {{planSelected.name}} ($ {{planSelected.price}})
        </div>
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
                }
            ],
            planSelected: null
        }
    },
    methods: {
        togglePlanSelected(plan) {
            this.planSelected = plan.isSelected ? plan : null;
        },
        isPlanSelected(plan) {
            if (this.planSelected && this.planSelected.name === plan.name) {
                return true;
            } else {
                return false;
            }
        }
    }
}
</script>

<style scoped>
.container {
	display: flex;
}

.item {
	flex-grow: 1;
}

.item+.item {
	margin-left: 2%;
}

.item.selected {
	background-color: rgba(0, 0, 0, 0.4);
}

.summary {
	color: #98a04f;
	font: normal 0.75rem Arial, Helvetica, Sans-serif;
	text-align: center;
	margin: 3rem 0;
	padding: 2rem;
	background: rgba(0, 0, 0, 0.25);
	border-radius: 3px;
}
</style>