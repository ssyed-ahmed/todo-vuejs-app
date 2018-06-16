<template>
  <div class="">
    <input type="text" class="todo-input" placeholder="What needs to be done">
    <div class="" v-for="(todo, index) in todos">
      {{ todo.title }}
    </div>
  </div>
</template>

<script>

export default {
  name: 'todo-list',
  data() {
    return {
      todos: [
        {
          title: 'Start learning vuejs',
          completed: false
        },
        {
          title: 'Implement a simple vuejs app',
          completed: false
        }
      ]
    }
  }
}

</script>

<style lang="scss">

</style>
