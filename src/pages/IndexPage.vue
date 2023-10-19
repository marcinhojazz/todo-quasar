<template>
  <q-page class="flex h-screen flex-center">
    <div class="space-y-2 px-64 w-full h-full text-center text-2xl text-white bg-gray-800">
      <h2>Welcome Todo List Quasar</h2>
      <div class="bg-slate-200 flex p-6">
        <p>1 - </p>
        <p>Task 1</p>
      </div>
      <div class="bg-slate-200 flex p-6">
        <p>1 - </p>
        <p>Task 1</p>
      </div>
      <div class="bg-slate-200 flex p-6">
        <p>1 - </p>
        <p>Task 1</p>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
