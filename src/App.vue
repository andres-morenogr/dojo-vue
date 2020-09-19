<template>
<v-app>
  <Toolbar/>
  <v-main>
    <Search v-on:searchResult="searchResult"/>
    <ImageList v-bind:items="items"/>
  </v-main>
</v-app>
</template>

<script>
import Toolbar from './components/ToolBar'
import Search from './components/Search'
import ImageList from './components/ImageList'

export default {
  name: 'App',

  components: {
    Toolbar,
    Search,
    ImageList
  },
  methods: {
    searchResult(result){
      this.items = result;
      console.log(this.items);
    }
  },

  data: () => ({
    items: []
  }),
};
</script>
