<template>
  <div class="hello">
    <input v-model="words" type="text" />
    <h3>{{ words }}</h3>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      words: 'hello world',
    }
  },
}
</script>

<style scoped>
.home {
  margin: 0 auto;
  text-align: center;
  font-size: 20px;
}
</style>
