<template>
  <div class="dropdown">
    <label>{{ label }}</label>
    <select v-model="selectedOption">
      <option v-for="option in options" :key="option">{{ option }}</option>
    </select>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  props: {
    label: String,
    options: Array,
    value: String // A prop para controlar a opção selecionada
  },
  setup (props, { emit }) {
    const selectedOption = ref(props.value)

    // Função para lidar com mudanças na seleção
    const handleSelection = () => {
      emit('update:value', selectedOption.value)
    }

    return {
      selectedOption,
      handleSelection
    }
  }
}
</script>

<style scoped>
.dropdown {
  display: flex;
  flex-direction: column;
  margin-bottom: 10px;
}

label {
  margin-bottom: 5px;
}

select {
  width: 100%;
  padding: 5px;
}
</style>
