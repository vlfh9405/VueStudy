<script setup>
  import { computed, reactive } from 'vue';
    const state = reactive({
    mvpId:1,
    player : [
    {id : 0, name : "설악산",},
    {id : 2, name : "지리산",},
    {id : 15, name : "북악산",},
    {id : 18, name : "관악산",},
    {id : 26, name : "한라산",},
  ]
  })
  const mvpIdNum = (event) => {
  state.mvpId = Numver(event.target.value);
  if(!isNaN(state.mvpId)) {
    state.mvpId = state.mvpId;
    console.log(state.mvpId);
  } 
};
  const mvpName = computed(()=>{
      const player = state.player.find(player => player.id === state.mvpId);
      return player ? player.name : "찾는선수 없음"
  })

  // console.log(mvpName);
  // console.log(mvpIdName.value);
</script>

<template>
  <input type="text" v-model.number="state.mvpId" @change = "mvpIdNum"/>
  <!-- <button @click ="mvpIdNum()">MVP 선수 ID : {{ state.mvpId }}</button> -->
  <h2>오늘의 MVP</h2>
  <div>MVP 선수 이름 : {{ mvpName }}</div>
</template>

<style scoped>

</style>