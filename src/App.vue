<template>
  <v-app>
    <Toolbar />
      <v-main>
      <Search v-on:searchResult="searchResult"/>
      <Imagen v-bind:items="items"/>
      </v-main>
  </v-app>
</template>

<script>
import Toolbar from './components/Toolbar';
import Search from './components/Search';
import Imagen from './components/Imagen';

export default {
  name: 'App',

  components: {
    Toolbar,
    Search,
    Imagen,
  },
  methods:{
    searchResult(response){
        this.items=response;
    }
  },
  data: () => ({
    items:[],
  }),
};
</script>
