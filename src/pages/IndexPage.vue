<template>
  <q-page class="flex h-screen flex-center">
    <div class="space-y-2 px-64 w-full h-full text-center text-2xl text-black bg-gray-200">
      <h2>Welcome Todo List Quasar</h2>
      <div>
        <MyButton label="Click Aqui"/>
        <MyInput v-model="inputValue" placeholder="Digite algo" />
        <MyCheckbox v-model="isChecked" label="Marque esta opção" />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import MyButton from '../components/atoms/MyButton.vue'
import MyInput from '../components/atoms/MyInput.vue'
import MyCheckbox from '../components/atoms/MyCheckbox.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    MyButton,
    MyInput,
    MyCheckbox
  },
  data () {
    return {
      inputValue: ''
    }
  }

})
</script>
