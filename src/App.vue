<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import QueryBox from './components/QueryBox.vue';
</script>

<template>
  <header>
    <h1>Narratrice</h1>
    <div>assaultlily-rdf simple frontend</div>
  </header>
  <QueryBox/>
  <div>
    ここに結果セットを吐き出すやつをつくるよ
  </div>
</template>

<style>
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0;
}

header {
  display: flex;
  align-items: baseline;
  background: linear-gradient(#94D7FF, skyblue);
  padding: 3px 10px;
  font-size: 17px;
}
header > h1 {
  margin: 0 10px 0 0;
  font-size: 20px;
}
</style>
