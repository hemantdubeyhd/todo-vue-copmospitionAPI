<template>
  <h1> Vue Compositon API Todo</h1>

  <input v-model="newItem" ref="itemInput" placeholder="Enter the new item.."/>
  <button @click="addItem">Add</button>

  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{ item }}
      <button @click="removeItem(index)">X</button>
    </li>
  </ul>
  </template>



  <script setup>
  import {ref, nextTick} from 'vue';

  const itemInput = ref(null);
  const newItem = ref('');
  const items = ref([]);

  const addItem = () => 
  {
      if(newItem.value.trim() != '')
    {
      items.value.push(newItem.value.trim());
      newItem.value = '';
      
      
    }

  };

  const removeItem = (index) => 
  {
    items.value.splice(index, 1);
  };
</script>
