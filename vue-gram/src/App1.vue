<template>
<div>
  <h1>Hello {{ animal }} </h1>
  <h2>Monkey likes {{food}}</h2>
  <input type="text" v-model="food"/>
  <br>
  <a :href="food">{{food}}</a>
  <h2 :class="{orange: food==='orange', 'not-good': food === 'choco'}">원숭이는 {{food}} 좋아함</h2>
  <!-- <img v-bind:src="imageSource" alt="random"/><br> -->
  <!-- <a :href="naverUrl">naver</a> -->
  <!-- <h3 v-text="food" v-model=""></h3> -->
  <!-- <div v-html="alertMessage"></div> -->
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      animal: "Monkey",
      food: "apple",
      imageSource: "https://placeimg.com/100/100/any",
      naverUrl: "https://www.naver.com",
    }
  }

}
</script>

<style>
.orange{
  color: orange;
}

.salmon{
  color: salmon;
}

.blue {
  color:blue;
}

.not-good {
  color: red;
  text-decoration: line-through;
}

</style>