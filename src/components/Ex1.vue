<script setup>

import { ref } from 'vue';

const id = ref('circle')


function mOver() {
    // add code here
    // alert("mOver!");
    
    id.value = "square";
    // note CSS & JS has no direct acknowledgement inside the <style>, 
    // you need to use quotations to the HTML element's id attribute
    
}

function mOut() {
    // add code here
    // alert("mOut!");
    id.value = "circle";
}
</script>

<template>
    <!-- modify code below -->
    <div :id="id"@mouseover=mOver @mouseout=mOut>
        Mouse Over Me
    </div>

</template>

<style scoped>
#square {
    width: 150px;
    height: 150px;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

#circle {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}
</style>