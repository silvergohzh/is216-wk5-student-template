<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here
const newItem = ref("");

function addItem() {
    if(newItem.value.trim() !== "") {
        items.value.push(newItem.value);
        newItem.value = '';
    }
}

// splice is to remove item
// splice(startIndex, deleteCount)
function removeItem(idx) {
    items.value.splice(idx, 1);
}

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->

    <ul>
        <li v-for="(item, idx) in items">
            {{item}}
            <button @click="removeItem(idx)">Delete!</button>
        </li>
    </ul>

    <input type="text" v-model="newItem">
    <button @click="addItem" >Add!</button>
   
    
</template>

