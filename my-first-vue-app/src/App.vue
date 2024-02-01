<template>
  <div class="container">
    <h1>Counter App</h1>
    <h2 :style="{ fontSize: fontSize + 'px', color: 'white' }">{{ counter }}</h2>
    <div class="buttons">
      <button @click="counter++">INCREMENT</button>
      <button @click="counter--">DECREMENT</button>
      <button @click="fontSize += 5">INCREMENT FONT</button>
      <button @click="fontSize -= 5">DECREMENT FONT</button>
    </div>
  </div>
</template>

<style>
* {
  font-family: sans-serif;
  box-sizing: border-box;
}

.container {
  margin-top: 50px;
  text-align: center;
  background-color: #2c3e50;
  /* Dark background color */
  padding: 20px;
  border-radius: 10px;
}

h1,
h2 {
  color: #ecf0f1;
  /* Light text color */
}

.buttons {
  display: flex;
  justify-content: center;
  flex-direction: column;
  gap: 10px;
}

button {
  font-size: 20px;
  padding: 10px 20px;
  background-color: #3498db;
  /* Button color */
  color: #ecf0f1;
  /* Button text color */
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #2980b9;
  /* Darker button color on hover */
}
</style>

<script setup>
import { ref } from 'vue';

const counter = ref(0);
const fontSize = ref(15);
</script>
