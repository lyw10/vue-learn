<template>
    <form @submit.prevent="addTodo" class="input-add">
        <input v-model="newTodo" type="text" name="todo" />
        <button type="submit">
          <i class="plus"></i>
        </button>
    </form>
</template>

<script>
export default {
    name:"todoadd",
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
.input-add{
  margin: 28px 0;
  position: relative;
}

.input-add input {
  width: 100%;
  height: 40px;
  border-radius: 20px;
  border: 0;
  outline: none;
  padding: 0 20px;
  box-shadow: 0px 0px 24px rgba(0, 0, 0, 0.08);
  color: #626262;
  font-size: 16px;
}

.input-add button{
  position: absolute;
  right: 0;
  width:40px;
  height: 40px;
  border-radius: 50%;
  border: 0;
  outline: none;
  background: linear-gradient(#c0a5f3, #7f95f7);
  color: white;
  cursor: pointer;
}

.input-add .plus{
  display: block;
  width: 100%;
  height: 100%;
  background: linear-gradient(#fff, #fff), linear-gradient(#fff, #fff);
  background-size: 50% 2px, 2px 50%;
  background-position: center;
  background-repeat: no-repeat;
}
</style>