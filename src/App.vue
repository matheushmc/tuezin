<script setup>
import {ref, computed} from 'vue'

const contador1 = ref(0)
const contador2 = ref(0)
const soma = computed (() => contador1.value + contador2.value)
</script>

<template>
 
 <div>
<button class="btn btn-primary" @click="contador1++">
  +
</button>
<span class="ex-3 fs-4">
  {{contador1 }}
</span>
<button class="btn btn-primary" @click=" contador1--">
  -
</button>
 </div>
 <div>
<button class="btn btn-primary" @click="contador2++">
  +
</button>
<span class="ex-3 fs-4">
  {{contador2 }}
</span>
<button class="btn btn-primary" @click=" contador2--">
  -
</button>
<div>
  <p class="fs-4">
    a soma dos dois é {{ soma }}
  </p>
  <div v-if="soma > 10 " class="fs-4" >
  a soma é maior que 10
  </div>
  <div v-else class="fs-4" >
  a soma é menor que 10
  </div>
 <div v-if="soma %2 === 0" class="fs-4">
  
 </div>
 <div></div>
 <div class="containers">
  <div class="btn btn-primary">
    OK
  </div>
 </div>
</template>

<style scoped>

</style>
