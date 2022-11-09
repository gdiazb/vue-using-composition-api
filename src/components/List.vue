<template>
  <ul class="list">
    <ItemList 
      v-for="(item, index) in tweeps"
      :key="index"
      :tweepTitle="item.tweepTitle"
      :tweepDescription="item.tweepDescription"
    />
    <p>Agrega un Tweep</p>
    <input
      type="text"
      placeholder="escriba un título"
      v-model="newTitle"
    >
    <input
      type="text"
      placeholder="escriba una descripción"
      v-model="newDescription"
    >
    <button @click="testEjm">Enviar</button>
  </ul>
</template>

<script setup>
import ItemList from './ItemList.vue'
import { reactive, ref } from 'vue'

const tweeps = reactive([])

const newTitle = ref('');
const newDescription = ref('');

const resetform = () => {
  newTitle.value = ''
  newDescription.value = ''
}

const testEjm = () => {
  tweeps.push({
    tweepTitle: newTitle.value,
    tweepDescription: newDescription.value 
  })
  resetform()
}
</script>