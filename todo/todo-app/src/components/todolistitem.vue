<template>
  <div class="todo-item">
    <label>
    <input type="checkbox">
    {{ todo.title }}
    <span class="check-button"></span>
    </label>
</div>
</template>

<script>
export default {
    name:"todolistitem",
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
    .todo-item{
  margin-bottom: 10px;
  background-color: white;
  border-radius: 10px;
  min-height: 40px;
  padding-left: 10px;
  display: flex;
  justify-content: start;
  align-items: center;
  color: #626262;
}

.todo-item label{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: start;
  cursor: pointer;
  position: relative;
}

.todo-item.done label{
  text-decoration: line-through;
  font-style: italic;
}

.todo-item label span.check-button{
  position: absolute;
  top: 0;
}

.todo-item label span.check-button::before,
.todo-item label span.check-button::after {
  content: "";
  display: block;
  position: absolute;
  width: 18px;
  height: 18px;
  border-radius: 50%;
}

.todo-item label span.check-button::before {
  border: 1px solid #b382f9;
}

.todo-item label span.check-button::after {
  transition: 0.4s;
  background: #b382f9;
  transform: translate(1px, 1px) scale(0.8);
  opacity: 0;
}

.todo-item input{
  margin-right: 16px;
  opacity: 0;
}

.todo-item input:checked + span.check-button::after {
  opacity: 1;
}
</style>