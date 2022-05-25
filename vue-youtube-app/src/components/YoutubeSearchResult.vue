<template>
  <div>
    <h2>검색 결과</h2>
    <div v-if="searchViedos.length">
      <ul>
        <li v-for="video in searchViedos" :key="video.id.videoId">
          <img :src="video.snippet.thumbnails.default.url" alt="">
          {{ video.snippet.title }}
        </li>
      </ul>
    </div>
    <div v-else>
      <h4>검색 결과가 없습니다.</h4>
    </div>
  </div>
</template>

<script>
import {mapState} from 'vuex'
export default {
  computed: {
    ...mapState([
      'searchViedos'
    ])
  }
};
</script>

<style></style>
