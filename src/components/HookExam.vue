<script setup>
import { onMounted, onUpdated, reactive } from 'vue';
// 생성 훅(hook) : 컴포넌트가 처음 생성될 때 실행되는 훅
// 상태 값을 초기화 하거나 데이터를 조회하는 로직

// 생성 훅 
// con hook = "onCreated";
// console.log(hook);st
(async function onCreated() {
  const hook = "onCreated";
  console.log(hook);
  console.log(document.querySelector("#test"));
})();
// 마운트 훅(mount hook) : 마운트가 완료된 후에 실행되는 훅
// mount : 컴포넌트를 DOM에 연결하고 화면에 출력하는 과정을 의미
onMounted(
  () => {
    console.log(document.querySelector("#test"));
  }
)
// 반응형 상태(state)
const state = reactive({message:"Hello Vue"});
// 업데이트 훅(update hook) : 반응형 상태의 데이터가 바뀌고, 화면(DOM)이 업데이트 되면
// 실행 되는 훅() 
onUpdated( () =>{
    console.log(document.querySelector("#test").innerText);
    console.log(document.getElementById("update").innerText);
});
</script>

<template>
  <h1>HookExam</h1>
  <div id ="test">즐거운 시간~~</div>
  <button id = "update" @click="state.message = '안녕' ">{{ state.message }}</button>
</template>

<style scoped>

</style>