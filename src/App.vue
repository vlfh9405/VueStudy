<script setup>
// import HelloWorld from "./components/HelloWorld.vue";
// import TestVue from "./components/TestVue.vue";
// import DirectiveExam from "./components/DirectiveExam.vue"; 
// import Login from "./components/Login.vue";
// import Conditional from "./components/Conditional.vue";
// import Loop from "./components/Loop.vue";
// import StateExam from "./components/StateExam.vue";
// import MvpName from "./components/Mvpname.vue";
// import HookExam from './components/HookExam.vue';
import Greeting from './components/Greeting.vue';
import { reactive } from 'vue';

const state = reactive({
  visible : true
})

</script>

<template>
  <h1>Vue 연습 app 부분</h1>
  
  <!-- props로 color를 설정해서 자식 컴포넌트에 넘겨주기 -->
  <!-- <HelloWorld color="red"/> -->
  <!-- <TestVue/> -->
  <!-- <DirectiveExam /> -->
  <!-- <Login/> -->
  <!-- <Conditional /> -->
  <!-- <Loop /> -->
  <!-- <StateExam /> -->
  <!-- <MvpName /> -->
  <!-- <HookExam /> -->
  <button v-if = "state.visible" @click = "state.visible = false">false</button>
  <button v-if = "!state.visible" @click = "state.visible = true">true</button>
  <Greeting v-if="state.visible"/>
</template>

<style scoped>

</style>
 