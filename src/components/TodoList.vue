<template>
  <div>
    <Input :value="todo"
           v-model="todo"
           placeholder="TODO Eg. `Got to do stuff`.. Press enter to add."
           @on-enter="addTodo"/>
    <Table :columns="columns" :data="data"></Table>
  </div>
</template>

<script>

  export default {
    name: "todoList",
    data() {
      return {
        todo: "",
        columns: [
          {title: 'Todo', key: 'todo'},
          {title: 'Status', key: 'status'}
        ],
        data: [
          {todo: 'Hello', status: 'Done'},
          {todo: 'World', status: 'Pending'},
        ]
      }
    },
    methods: {
      addTodo: function () {
        this.data.push({todo: this.todo, status: 'Pending'});
        this.todo = "";
      }
    }
  }
</script>
