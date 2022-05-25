<template>
  <div>
    <h2>검색</h2>
    <input type="text" v-model="keyword">
    <button @click="search">검색</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      keyword:''
    }
  },
  methods: {
    search() {
      this.$store.dispatch("searchYoutube", this.keyword)
    }
  }

};
</script>

<style></style>
