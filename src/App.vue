<script setup>
import { reactive, ref } from 'vue'

const awesome = ref(true) 
const count = ref(0)
const text = ref('')


function increment(){
  count.value++
}

function klik() {
  awesome.value = !awesome.value
}


</script>
<template>
  <input v-model="text" placeholder="type here">
    <p>{{ text }}</p>
      <button @click="klik">klik</button>
      <h3>
      <button @click="increment">input: {{ count }}</button>
      </h3>
    <h1 v-if="awesome">saya berhasil menyelesaikannya</h1>
    <h1 v-else>saya tidak bisa menyelesaikannya</h1>
</template>
