<template>
  <div id="app">
    <h1>Hello, Vue!</h1>
    <TodoList />
  </div>
</template>

<script>
import TodoList from './TodoList.vue';

export default {
  name: 'App',
  components: {
    TodoList
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>