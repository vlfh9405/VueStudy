<!-- SFC(Single File Component) : 하나의 파일에 템플릿, 스크립트, 
 스타일 블록이 함께 정의되어 있는 구조 -->

<script setup>
 /*
    자바스크립트 코드를 입력, 일반적으로 코드 상단에 위치 setup  속성을 통해 이
    스크립트 코드가 setup hook임을 명시
  */
  const message = "Hello~!"
</script>

<template>
  <div class = "TestVue">
    <h1>TestVue Page</h1>
    <h2>{{message}}</h2>
  </div>

</template>

<style scoped>
/*  scoped : 해당 스타일이 이 컴포넌트에서만 적용된다.
    일반적으로 하단에 위치 시킨다. 
*/
.TestVue{
  max-width: 500px;
  width: 100%;
  background-color: rgb(221, 221, 221);
  max-height: 100vh;
  height: 500px;
  margin: auto;
}
</style>