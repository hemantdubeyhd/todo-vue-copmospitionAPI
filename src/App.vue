<template>
  <h1> Vue Compositon API Todo</h1>

  <input v-mode="newItem" placeholder="Enter the new item.."/>
  <button @click="addItem">Add</button>

  <ul>
    <li v-for="(item, index)" in items :key="index">
      {{ item }}
      <button @click="removeItem(index)">X</button>
    </li>
  </ul>
  </template>
  