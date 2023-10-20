<template>
  <q-btn
    :color="buttonColor"
    :outline="outline"
    @click="$emit('click')"
  >
    {{ label }}
  </q-btn>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    label: String,
    buttonColor: String,
    outline: Boolean
  }
}
</script>
