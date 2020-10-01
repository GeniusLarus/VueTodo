<template>
  <form @submit.prevent="onSubmit">
    <input type="text" name="New task" v-model="title">
    <button type="submit">Create</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: ''
    }
  },
  methods: {
    onSubmit() {
      if (this.title.trim()) {
        const newTodo = {
          id: Date.now(),
          title: this.title,
          completed: false
        }
        this.title = '';
        this.$emit('add-todo', newTodo)
      }
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: 100%;
  }
  input {
    width: 80%;
    padding: .5rem 2rem;
    margin-bottom: 1rem;
    border: 1px solid #ccc;
  }
  button {
    padding: .5rem 2rem;
    margin-bottom: 1rem;
    border: 1px solid #ccc;
  }
</style>