<template>
<div class="home">
  <div class="count">{{ storeCounter.count }}</div>
  <div class="buttons">
    <button @click="storeCounter.decreaseCount">-</button>
    <button @click="storeCounter.increaseCount">+</button>
  </div>
  <hr>
  <div>The counter is {{ storeCounter.oddOrEven }}</div>
  <hr>
  <h3>Edit counter:</h3>
  <input
  v-model="storeCounter.count"
  type="number"
  />
</div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter'

const storeCounter = useCounterStore()

</script>

<style>
.count {
  font-size: 60px;
  margin: 20px;
}

.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>
