<template>
  <button :class="buttonClass" @click="handleClick">
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: String,
    buttonColor: String // Nova prop para especificar a cor do botão
  },
  setup (props, { emit }) {
    const buttonClass = `custom-button ${props.buttonColor || 'default'}`

    const handleClick = () => {
      emit('click')
    }

    return {
      buttonClass,
      handleClick
    }
  }
}
</script>

<style scoped>
.custom-button {
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 4px;
}

.default {
  background-color: #ccc;
  color: #333;
}

.primary {
  background-color: #007bff;
  color: #fff;
}
.secondary {
  background-color: #26A69A;
  color: #fff;
}
.amber {
  background-color: #F2C037;
  color: #fff;
}
.warning {
  background-color: #f23737;
  color: #fff;
}
</style>
