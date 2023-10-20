<template>
  <q-page class="flex h-screen flex-center">
    <div class="space-y-2 px-6 lg:px-64 w-full h-full text-center text-2xl text-black bg-gray-200">
      <h2>Welcome Todo List Quasar</h2>
      <div>
        <div>
          <p class="text-left">Buttons Pure Vue</p>
          <div class="flex gap-2">
            <VButton
              label="Primary"
              buttonColor="primary"
            />
            <VButton
              label="Secondary"
              buttonColor="secondary"
            />
            <VButton
              label="Amber"
              buttonColor="amber"
            />
            <VButton
              label="Standard Outline"
              buttonColor="warning"
            />
            <span>...</span>
          </div>
        </div>
        <MyInput v-model="inputValue" placeholder="Digite algo" />
        <MyCheckbox v-model="isChecked" label="Marque esta opção" />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import VButton from '../components/atoms/VButton.vue'
import MyInput from '../components/atoms/MyInput.vue'
import MyCheckbox from '../components/atoms/MyCheckbox.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    VButton,
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
