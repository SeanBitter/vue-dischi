<template>
  <div id="app">
    <SearchBar :genres-list="genresList"></SearchBar>
    <AlbumsList/>
  </div>
</template>

<script>
import AlbumsList from './components/AlbumsList.vue'
import SearchBar from './components/SearchBar.vue'
// import { state } from "./store";

export default {
  name: 'App',
  components: {
    AlbumsList, SearchBar
  },
  data() {
    return {
      genresList: [],
      genre: "",
    }
  }
}
</script>

<style lang="scss">
@import "assets/scss/main.scss";

</style>
