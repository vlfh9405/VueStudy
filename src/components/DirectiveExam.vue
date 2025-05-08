<script setup>
const message = "Hello Vue";
const vtest = {
  name : "홍길동",
  age : 20,
};
const direct = "direct_exam";
</script>

<template>
  <div v-bind:id = "direct">
    <h1> {{ message }} </h1> 
    <span>안녕</span>
    <span v-text = "message"></span><br/>
    <hr/>
    <div v-text = "vtest.name"></div>
    <div v-text = "vtest.age"></div>
    <div v-text = "vtest"></div>
    <div v-text = "vtest.name + '님은 '+ vtest.age + '세 입니다.'"></div>
    <div v-text = "`${vtest.name} 님은 ${vtest.age} 세 입니다.`"></div>
    <!-- JSON 파일로 출력  
         JavaScript Object Notation : 문자열 기반의 데이터 형식
         서로다른 서비스나 애플리케이션 간의 데이터 저장과 교환에 사용 
    --> 
    <div v-text = "JSON.stringify(vtest)"></div>

  </div>
</template>

<style scoped>
  #direct_exam{
     color:blue;
     font-family : "궁서체";
  }
</style>