<script setup lang="ts">
import {ref} from "vue"
const data = ref('')
const push = () => {
  console.log(data.value)
}
const clean = () => {
  data.value = ""
}
</script>

<template>
  <n-flex>
    Native
    <input class="Test" type="text" v-model="data" />
    <n-space>
      <button @click="clean">Clean</button>
      <button @click="push">Log</button>
    </n-space>
  </n-flex>
  <n-flex>
    Framework
    <n-input class="Test" type="text" v-model:value="data" />
    <n-space>
      <button @click="clean">Clean</button>
      <button @click="push">Log</button>
    </n-space>
  </n-flex>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
