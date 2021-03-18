<template>
  <main>
    <div class="container">
      <h1>鱼尾的Deadline</h1>
      <todoadd />
      <todofliter />
      <todolist />
    </div>
  </main>
</template>

<script>
import todoadd from './components/todoadd.vue'
import todofliter from './components/todofliter.vue'
import todolist from'./components/todolist.vue'


export default {
  components: { todoadd,todofliter,todolist},
  name: 'App'
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

main{
  width: 100vw;
  min-height: 100vh;
  padding: 10vh 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #d8dfff;
}

.container{
  background-color: rgb(245, 246, 252);
  box-shadow: 0 0 24px rgba(0,0,0,.15);
  border-radius: 24px;
  width: 60%;
  max-width: 400px;
  padding:  48px 28px;
}

h1{
  font-size: 1.75rem;
  letter-spacing: 0.25rem;
  color: #414873;
}
</style>
