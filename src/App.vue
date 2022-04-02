<script setup>
import BaseButton from './components/BaseButton.vue'
import { ref } from 'vue'
const yText=ref('This is button');
const yColor=ref('#00000')
</script>
 
<template>
  <div>
    <div>Your Text:<input type="text" v-model="yText"></div>
    <BaseButton :yourText="yText"></BaseButton>
    <div>
      Your Color:{{ yColor }}<input type="color" v-model="yColor">
    <BaseButton :yourText="yText" :yourColor="yColor"></BaseButton>

    </div>
  </div>
</template>
 
<style>

</style>