<template>
  <q-btn
    color="primary"
    @click="$emit('click')"
  >
    {{ label }}
  </q-btn>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    label: String
  }
}
</script>
