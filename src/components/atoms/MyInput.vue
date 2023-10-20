<template>
  <q-input
    v-model="inputValue"
    @input="$emit('input', inputValue)"
    :placeholder="placeholder"
  />
</template>

<script>
export default {
  name: 'MyInput',
  props: {
    value: String,
    placeholder: String
  },
  data () {
    return {
      inputValue: this.value
    }
  }
}
</script>
