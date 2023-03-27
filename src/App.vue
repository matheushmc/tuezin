<script setup>
import {ref, computed} from 'vue'
const contador1 = ref(0)
const contador2 = ref(0)
const soma = computed(() => contador1.value + contador2.value)
const mostrar = ref(true)
</script>

<template>
  <div class="container">
    <div class="mt-4">
      <div class="mt-4">
        <button class="btn btn-primary" @click="mostrar = !mostrar">
          *
        </button>
      </div>
      <div v-if="mostrar" class="mt-4">
        <button class="btn btn-primary" @click="contador1--">
          -
        </button>
        <span class="ex-3 fs-4">
          {{ contador1 }}
        </span>
        <button class="btn btn-primary" @click="contador1++">
          +
        </button>
      
      <div>
        <button class="btn btn-primary" @click="contador2--">
          -
        </button>
        <span class="ex-3 fs-4">
          {{ contador2 }}
        </span>
        <button class="btn btn-primary" @click="contador2++">
          +
        </button>
      </div>
      <div>
        <p class="fs-4">
          A soma dos dois é {{ soma }}
        </p>
        <div v-if="soma > 10" class="fs-4">
          A soma é maior que 10
        </div>
        <div v-else class="fs-4">
          A soma é menor que 10
        </div>
        <div v-if="soma %2 === 0" class="fs-4">
          A soma é par
        </div>
        <div v-else class="fs-4">
          A soma é impar
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
</style>