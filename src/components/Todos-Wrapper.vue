
<template>
  <div class="todos__wrapper">
  <div class="todos__wrapper-input">
    <form action="submit" class="todos__wrapper-form">
      <input type="text" name="todo" id="todoInput" placeholder="Enter a new Task">
      <button type="button">Add</button>
    </form>
  </div>
   <TodosGrid/>
  </div>
</template>

<script>
import TodosGrid from './Todos-Grid.vue'
export default {
  name: 'TodosWrapper',
  components: {
    TodosGrid,
    

  }

}
</script>

Add "scoped" attribute to limit CSS to this component only
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
