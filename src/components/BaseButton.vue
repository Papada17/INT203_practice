<script setup>
import { computed } from '@vue/reactivity';
const prop = defineProps({
    yourText:{
        type:String,
        require:true
    },
    yourColor:{
        type:String,
        require:true
    }
})
// const buttonText = ref(prop.yourText) //ปุ่มไม่สามารถเปลี่ยนตามinputได้
//const buttonText = computed(()=>prop.yourText) //computed เปลี่ยนไปตาม original ที่เปลี่ยน
</script>
 
<template>
<!-- <div>
    <button>{{ buttonText }} </button>
</div> -->
<div>
    <button class="button-color">{{ yourText }}</button>
</div>
</template>
 
<style>
.button-color{
    background-color: v-bind(yourColor);
}
</style>