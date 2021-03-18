<template>
  <div class="todo-list">
        <todolistitem v-for="todo in todos" :key="todo">
        </todolistitem>
    </div>
</template>

<script>
import todolistitem from './todolistitem.vue'
export default {
    name:"todolist",
    components: {todolistitem},
    data(){
    return {
      newTodo: '',
        todos: []
      }   
    },
    methods: {
        addTodo() {
            this.todos.push({
                title: this.newTodo,
                done: false
            })
            this.newTodo = ''
        }
    }
}
</script>

<style>

</style>