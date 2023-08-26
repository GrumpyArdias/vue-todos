
<template>
  <div class="todos__wrapper">
  <div class="todos__wrapper-input">
    <form action="submit" class="todos__wrapper-form">
      <input type="text" name="todo" id="todoInput" placeholder="Enter a new Task" v-model="todoInput">
      <button id="todosAddButton" @click="addTodo" type="submit">Add</button>
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
  },
  data (){
    const storedTodos = localStorage.getItem("todos");
    return{
      todos: storedTodos ? JSON.parse(storedTodos) : [],
      todoInput: ''
    }
  },
  methods: {
    addTodo: function(){
      console.log(JSON.stringify(this.todos))
      // this.todos= [...this.todos,this.todoInput]
      this.todos.push(this.todoInput)
      localStorage.setItem("todos", JSON.stringify(this.todos))
      console.log(JSON.stringify(this.todos))
      this.todosInput = ''
    }
  }
}
</script>

