<template>
  <div>
    <ul>
      <li class="flex row items-center justify-between w-full
      py-1 px-4 my-1 rounded border bg-gray-100 text-gray-600"
      v-for="(todoItem, index) in todoItems" :key="todoItem">
        <div class="items-center flex-row">
          <span class="float-right px-4 py-2">
            <i class="fas fa-check"></i>
          </span>
        </div>
        {{ todoItem }}
        <div class="items-center flex-row-reverse"
        v-on:click="removeTodo(todoItem,index)">
          <span class="float-right px-4 py-2">
            <i class="fas fa-times"></i>
          </span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TodoList",
  props: ['todoItems'],
  methods: {
    removeTodo(todoItem, index) {
      this.$emit('removeTodo', todoItem, index);
    }
  }
}
</script>

<style scoped>

</style>
