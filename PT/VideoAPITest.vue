<template>
  <div class = "exer-video">
      <h1>
        <v-icon x-large
        color = gray
        > mdi-lightbulb-alert</v-icon>
        오늘의 추천 영상
        </h1>
      <br>
       <v-card
    class="mx-auto"
    max-width="700"
  >
  <v-for ="video in videos">{{ video }}</v-for>
   

    <v-card-title>
      Top western road trips
    </v-card-title>

    <v-card-subtitle>
      1,000 miles of wonder
    </v-card-subtitle>
        <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn
        icon
        @click="show = !show" 
      >
    <v-icon
    large
    color = red
    > mdi-heart-plus</v-icon>
      </v-btn>


    </v-card-actions>
  </v-card>

  <br>
  <br>
       <v-card
    class="mx-auto"
    max-width="700"
  >
    <v-img
      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
      height="400px"
    ></v-img>

    <v-card-title>
      Top western road trips
    </v-card-title>

    <v-card-subtitle>
      1,000 miles of wonder
    </v-card-subtitle>  
    <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn
        icon
        @click="show = !show" 
      >
    <v-icon
    large
    color = red
    > mdi-heart-plus</v-icon>
      </v-btn>


    </v-card-actions>
  </v-card>
    

  </div>
</template>

<script>
import axios from 'axios';

export default {
   data: () => ({
      show: true,
      videos: [],
    }),
  created() {
    axios.get("https://api.hnpwa.com/v0/news/1.json")
    .then(response => this.movies = response.data)
    .catch()
  },
}
</script>

<style>

</style>