<template>
    <div class="item" @click="toggleSelectPlan" :class="{'selected':isSelected}">
        <h3>{{name}}</h3>
        <h4><span>$ </span>{{price}}<span><em> / year</em></span></h4>
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
        isSelected: Boolean
    },
    methods: {
        toggleSelectPlan: function() {
            this.isSelected = !this.isSelected;
            this.$emit('toggleSelect', this);
        }
    }
}
</script>
<style scoped>
div {
	background: rgba(0, 0, 0, 0.2);
	padding: 15px;
	text-align: center;
	border-radius: 5px;
	color: #98a04f;
	user-select: none;
	border: 6px dashed rgba(0, 0, 0, 0.2);
	box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.4);
}

div:hover {
	background-color: rgba(0, 0, 0, 0.3);
}

h3,
h4 {
	margin: 0;
}

h3 {
	margin-bottom: 1rem;
	padding-bottom: 0.9rem;
	border-bottom: 1px dashed #405468;
	text-transform: uppercase;
	font-size: .8rem;
}

h4 {
	font-weight: 600;
	font-size: 3rem;
}

h4 span {
	font-size: 1.5rem;
	font-weight: 400;
	vertical-align: middle
}
</style>