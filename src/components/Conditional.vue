<script setup>
  let loading = true;


</script>

<template>
  <div v-if = "loading">Loding...</div>
  <div v-else>로딩 완료</div>
  <hr/>
  <div v-show = "loading">
      <h3>로딩 중...</h3>
  </div>
  
  <div v-show = "!loading">


  </div>
</template>

<style scoped>

</style>