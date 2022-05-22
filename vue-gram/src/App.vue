<template>
  <div>
      <!-- <h1>{{count + 1}}</h1>
      <button v-on:click="addNumber(1)">증가</button>
      <button v-on:click="minusNumber">감소</button>
      <button v-on:mouseover="addNumber(10)">10씩증가</button> -->
      <h2>{{message}}</h2>
      <button @click="greeting">인사</button>
      <button @click="goodbye">작별</button>
      <br>
      <div @mouseover="getMouse" class="box"></div>
  </div>
</template>

<script>
export default {
    name: "App",
    data() {
        return {
            count: 0,
            message: "",
        }
    },
    methods: {
        getMouse(event) {
            this.message= `마우스의 위치 ${event.pageX}, ${event.pageY}입니다.`;
        },
        greeting() {
            this.message = "하이"
        },
        goodbye() {
            this.message= "빠이"
        },
        addNumber(value){
            //console.log("add Number")
            this.count = this.count + value;
        },
        // arrow -function은 인식을 못 한당
        minusNumber() {
            this.count = this.count - 1
        }
    },
};
</script>

<style>
button {
    width: 50px;
    height: 50px;
}
.box {
width: 300px;
height: 300px;
color: aliceblue
}
</style>