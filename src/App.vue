<template>
  <div id="app">
    <router-view>
      <todo-list slot="content"></todo-list>
    </router-view>
  </div>
</template>

<script>
  import TodoList from './components/TodoList.vue';

  export default {
    name: 'app',
    components: {TodoList}
  }
</script>

<style>
</style>
