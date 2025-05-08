<!-- 마운트 시키고 마운트 해제 
     마운트 해제 훅 : 컴포넌트가 소멸된 후에 실행되는 훅
-->
<script setup>
import { onMounted, onUnmounted } from 'vue';

onMounted( 
  () => {
    console.log("onMounted", document.querySelector("#greeting"));
  }
);
      
onUnmounted(
  ()=>{
    console.log("onUnmounted", document.querySelector("#greeting"));
  }
);

</script>

<template>
  <h1>Unmount 연습</h1>
  <div id ="greeting">안녕~~! 반가워~!</div>
</template>

<style scoped>

</style>