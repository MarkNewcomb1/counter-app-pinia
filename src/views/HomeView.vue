<template>
<div class="home">
  <div class="count">{{ count }}</div>
  <div class="buttons">
    <button @click="decreaseCount">-</button>
    <button @click="increaseCount">+</button>
  </div>
  <hr>
  <div>The counter is {{ oddOrEven }}</div>
</div>
</template>

<script setup>
import { ref, computed } from 'vue'

const count = ref(0);

function increaseCount() {
  count.value++;
}

function decreaseCount() {
  count.value--;
}

const oddOrEven = computed(() => {
  if (count.value % 2 === 0) return 'even'
  return 'odd'
})
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
