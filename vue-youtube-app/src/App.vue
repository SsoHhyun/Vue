<template>
  <div id="app">
    <h2>Youtube 검색 App</h2>
    <youtube-search></youtube-search>
    <youtube-search-result></youtube-search-result>
  </div>
</template>

<script>
import YoutubeSearch from './components/YoutubeSearch.vue'
import YoutubeSearchResult from '@/components/YoutubeSearchResult.vue'

export default {
  name: 'App',
  components: {
    YoutubeSearch,
    YoutubeSearchResult
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
