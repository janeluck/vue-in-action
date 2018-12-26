<template>
  <div class="todolist">
    <h1>TodoList</h1>
    <ul>
      <li  v-for="item in todos" :key="item.id">{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TodoList",
  props: {
    todos: Array
  }
};
</script>

<style>
</style>