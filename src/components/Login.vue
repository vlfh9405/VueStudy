<script setup>
  // const bind_exam = "sample";
  // const bind_exam2 = "sample exam1";
  // const bind_exam3 = ["sample", "exam1"];
  // const sample2 = "color:blue; border:1px solid red; height:50px";
  // const sample2 = {
  //   color : "blue", 
  //   border : "1px solid red", 
  //   height : "50px",
  //   };
    // const loading = true;
  import { reactive } from 'vue';
  const state = reactive({
    form : {id : "",
      pwd : "",
    }
  })
  const login = () => {
    console.log(state.form.id);
    console.log(state.form.pwd);
    alert(`${state.form.id}님 환영합니다.`);
    state.form.id = "";
    state.form.pwd = "";
  }
</script>

<template>
  <!-- v-bind 연습 -->
  <!-- <div :class ="bind_exam">안녕~!!!</div>
  <div :class ="bind_exam2">안녕~!!!</div>
  <div :class ="bind_exam3">안녕~!!!</div>

  <div :style ="sample2">안녕~!!!</div> -->
  <!-- <div>
    아이디  <input type="text" :readonly = "loading" placeholder = "아이디"/><br/>
    비밀번호 <input type="password" :disabled = "loading" placeholder = "비밀번호"/><br/>
    <button type = "button" :disabled = "loading" >로그인</button>
  </div> -->

  <div>
    <form @submit.prevent = "login">
      아이디  : <input type="text" v-model="state.form.id" placeholder = "아이디"/><br/>
      비밀번호 : <input type="password" v-model="state.form.pwd" placeholder = "비밀번호"/><br/>
      <button type = "submit" >로그인</button>
    </form>
  </div>
  <hr/>
  <h3>아이디 : {{ state.form.id }}</h3>
  <h3>비밀번호 : {{ state.form.pwd }}</h3>

</template>

<style scoped>
.sample{
  width: 300px;
  margin: auto;
  height: 50px;
  color: green;
  font-family: "궁서체";
}
.exam1{
  margin: 10px;
  color: blue;
  border: 1px solid green;
}
</style>