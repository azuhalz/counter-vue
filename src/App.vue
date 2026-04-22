<script setup>
import { ref } from "vue";
const count = ref(0);
function increase() {
  count.value++;
}
function decrease() {
  count.value--;
}
</script>

<template>
  <main>
    <div>
      <h1>Counter</h1>
      <span id="value">{{ count }}</span>
      <div>
        <button @click="decrease" id="decrease">-</button>
        <button @click="increase" id="increase">+</button>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  text-align: center;
  background-color: gray;
  padding: 20px;
  border-radius: 8px;
}

#value {
  font-size: 50px;
}

button {
  margin: 5px;
  padding: 10px 20px;
  font-size: 16px;
  border-radius: 4px;
  border: none;
  cursor: pointer;
  color: white;
  background-color: #555555;
}

button:hover {
  background-color: #777777;
}
</style>
