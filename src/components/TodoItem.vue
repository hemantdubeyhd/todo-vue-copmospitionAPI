<template>
    <li>
        {{ item }}
        <button @click="deleteItem">X</button>
    </li>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';
const props = defineProps({
    item: String,
    index: Number
});

const emit = defineEmits(['delete-Item'])

const deleteItem = () =>
{
    emit('delete-item', props.index);
}

</script>