<template>
  <div class="flex column">
    <input class="shadow appearance-none border rounded
    w-full py-2 px-3 text-gray-700 leading-tight text-center
    focus:outline-none focus:shadow-outline"
           type="text" placeholder="aaa"
    v-model="todoItem">
    <button class="bg-white hover:bg-gray-100 text-gray-800
    font-semibold py-2 px-4 border border-gray-300 rounded shadow ml-1"
            type="button"
    v-on:click="addTodo">
      <i class="fas fa-plus"></i>
    </button>
  </div>
</template>

<script>
export default {
  name: "TodoInput",
  data() {
    return {
      todoItem: '',
    }
  },
  methods: {
    addTodo() {
      if(this.todoItem !== ''){
        let value = this.todoItem.trim();
        this.$emit('addTodo', value);
      }

    }
  }
}
</script>

<style scoped>

</style>
