<template>
  <div>
    <button class="bg-white hover:bg-gray-100 text-gray-800 py-2 px-4
    border border-gray-300 rounded shadow ml-1" type="button"
    v-on:click="removeAll">
      Clear All
    </button>
  </div>
</template>

<script>
export default {
  name: "TodoFooter",
  methods: {
    removeAll() {
      this.$emit('removeAll');
    }
  }
}
</script>

<style scoped>

</style>
