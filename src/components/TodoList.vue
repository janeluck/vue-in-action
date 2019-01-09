<template>
  <div class="todolist">
    <h1>TodoList</h1>
    <input type="text" v-model="newTodo" @click="addTodo">
    <ul>
      <li  v-for="item in todos" :key="item.id">{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TodoList",
  props: {
    todos: Array,
    newTodo: String,
    addTodo: Function
  }
};
</script>

<style>
</style>