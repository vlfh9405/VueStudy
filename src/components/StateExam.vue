<script setup>
  import {ref, reactive} from 'vue';
  
  let count = ref(0);
  const counter = () => {
      count.value ++;
      console.log(`count : ${count.value}`)
  }

  let state = reactive({increCount : 0});
  const stateIncrease = () => {
    state.increCount ++;
    console.log(state.increCount);
  }
</script>

<template>
   <!-- <button v-on:click="counter()">{{  }}</button> -->
   <button @click="counter()">{{ count }}</button>
    <hr/>
   <div>
    <button @click = "stateIncrease()">reactive 활용 클릭</button>
    <h2>reactive 메서드를 활용한 상태 변화 : {{ state.increCount }}</h2>
   </div>
</template>

<style scoped>

</style>