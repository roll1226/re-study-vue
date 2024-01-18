<script setup lang="ts">
import { useCounterStore } from '@/stores/counter'
import { storeToRefs } from 'pinia'

const store = useCounterStore()
const { count, doubleCount } = storeToRefs(store)
const { increment } = store
</script>

<template>
  <div>
    <button @click="increment">+</button>
    <p>
      {{ count }}
    </p>
    <p>
      {{ doubleCount }}
    </p>
  </div>
</template>
