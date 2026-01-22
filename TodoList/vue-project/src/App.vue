<script>
import TodoHeader from './components/TodoHeader.vue';
import TodoInput from './components/TodoInput.vue';
import TodoList from './components/TodoList.vue';

  export default{
    components: {
      data(){
        return {
          todo: [],
          current: 'all',
        };
      },
      methods:{
        addTodo(inputMsg){
          const item = {
            id: Math.random(),
            msg: inputMsg,
            completed: false,
          };
          this.todo.push(item);
        },
      },
    }
  }
</script>
<template>
  <div class="todo">
    <TodoHeader :current="current"/>
    <TodoList />
    <TodoInput @add-todo="addTodo" />
  </div>
</template>