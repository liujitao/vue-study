<template>
  <div class="home">
    <TodoList />
  </div>
</template>

<script>
import TodoList from '../components/TodoList.vue'
import '../assets/style.css'

export default {
  name: 'Home',
  components: {
    TodoList,
  },
}
</script>
