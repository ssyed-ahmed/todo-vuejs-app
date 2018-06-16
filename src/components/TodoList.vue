<template>
  <div class="">
    <input type="text" class="todo-input" placeholder="What needs to be done" v-model="newTodo" @keyup.enter="addTodo">
    <div v-for="(todo, index) in todos" :key="todo.id" class="todo-item">
      {{ todo.title }}
    </div>
  </div>
</template>

<script>

export default {
  name: 'todo-list',
  data() {
    return {
      newTodo: '',
      idForTodo: 3,
      todos: [
        {
          id: 1,
          title: 'Start learning vuejs',
          completed: false
        },
        {
          id: 2,
          title: 'Implement a simple vuejs app',
          completed: false
        }
      ]
    }
  },
  methods: {
    addTodo() {
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false
      })
    }
  }
}

</script>

<style lang="scss">
.todo-input {
  width: 100%;
  padding: 10px 18px;
  font-size: 18px;
  margin-bottom: 16px;
}
.todo-item {

}
</style>
