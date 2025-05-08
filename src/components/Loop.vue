<script setup>
  const fruits = ["apple", "banana", "orange"];
  const students = [
    { id : 1, name : "홍길동", age : 20,},
    { id : 2, name : "김건호", age : 30,},
    { id : 3, name : "감자밭", age : 21,},
    { id : 3, name : "나오리", age : 22,},
  ]
  const test = () => {
    alert(students[1].name)
  }
</script>

<template>
  <button @click="test">버튼</button>
  <div v-for="fruit in fruits">
    <h2 >{{ fruit }}</h2>
  </div>
  <div v-for="(fruit, index) in fruits">
      <h2>{{ index + 1 }} 번 과일 : {{ fruit }}</h2>
  </div>
<!-- 각 항의 고유값을 key 속성으로 지정하면 데이터 변경에 더 효율적으로 대처가 가능 하다. -->
  <div v-for="student in students" :key = "student.id">
      <h2>{{ student.id }}  :  {{ student.name }} ΘωΘ {{ student.age }}</h2>
  </div>
</template>

<style scoped>
  h2{
    color: orange;
  }
</style>