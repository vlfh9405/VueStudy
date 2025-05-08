<script setup>
import "../assets/HelloWorld.css";

const msgText = "Hi Vue~?";
const props = defineProps({color : String});
</script>

<template>
  <div  class="HelloWorld">
    <!-- 머스태시 문법(mustache) : vue 에서 텍스트를 동적으로
     출력하는 방법으로 중괄호 두개 {{}} 를 이용 -->
    <h1>{{ msgText }}</h1>
    <!-- 디렉티브(directive) : 'v-' 로 시작하는 특수한 속성
     동적으로 텍스트를 출력하거나 클래스를 표시하고, 조건에 따라 일부 요소의 출력을 제어하거나
     반복하고, 이벤트를 다루는 역할
     v-bind : 속성 = "값"  => v-bind는 생략가능
     v-text : "값"
     v-if : 
     v-else : 
     v-show : 
     ... 
     -->
    <div :style="{color : props.color}">
      {{ props.color || "생삭없음" }}
    </div>
    <h1>즐거운 시간</h1>
  </div>
  </template>

<style scoped>
/* 외부에서 스타일 시트를 불러와서 적용할 경우
   같은 스타일일 경우 내부에서 정의한 스타일이 적용된다.
*/
.HelloWorld{
  margin: 0 auto;
  background-color: rgb(220,220,220);
  border: 1px solid black;
  width: 100%;
  max-width: 500px;
  box-shadow: rgb(220,220,220) 1px 1px 20px
}
</style>
