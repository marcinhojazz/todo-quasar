<template>
  <button @click="handleClick" class="custom-button">
    {{ label }}
  </button>
</template>

<script>
import { ref } from 'vue'

export default {
  props: {
    label: String
  },
  setup (props, { emit }) {
    const handleClick = () => {
      emit('click')
    }

    return {
      handleClick
    }
  }
}
</script>

<style scoped>
.custom-button {
  background-color: #007bff;
  color: #fff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 4px;
}
</style>
