<template>
  <label>
    <q-checkbox v-model="isChecked" @input="$emit('input', isChecked)" class="text-primary" />
    <span>{{ label }}</span>
  </label>
</template>

<script>
export default {
  name: 'MyCheckbox',
  props: {
    value: Boolean,
    label: String
  },
  data () {
    return {
      isChecked: this.value || false
    }
  }
}
</script>
