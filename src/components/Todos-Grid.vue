<template>
    <div class="todos-grid">
       <TodosCard /> 
    </div>
</template>

<script>
import TodosCard from './Todos-Card.vue';
export default {
    name: 'TodosGridt',
    components: {
        TodosCard,
    },
}
</script>
