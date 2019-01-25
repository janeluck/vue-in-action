<template>
  <div id="app">
  <!--   <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Awesome msg="Awesome jane" v-bind:btn="{name:'button01'}"/>
    <Sweet />
    <TodoList
            style="display: none"
    :add-todo="addTodo"
    newTodo="0" v-bind:todos="[{name: 'todo0', id: 't0'},{name: 'todo1', id: 't1'}]"/>
  </div>
</template>

<script>
//import HelloWorld from "./components/HelloWorld.vue";
import Awesome from "./components/Awesome.vue";
import TodoList from "./components/TodoList.vue";
import Sweet from "./components/Sweet.vue";

export default {
  name: "app",
  components: {
   // HelloWorld,
    Awesome,
    TodoList,
    Sweet
  },
  data: function () {
    return {
      addTodo: function () {

      }
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
