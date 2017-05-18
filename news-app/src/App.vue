<template>
  <div class="container" id="app">
    <!--main components-->
    <sourceSelection v-on:sourceChanged="sourceChanged"></sourceSelection>
    <newsList v-bind:source="source"></newsList>
  </div>
</template>

<script>
  //Importing the main components
import sourceSelection from './components/sourceSelection'
import newsList from './components/newsList'

export default {
  name: 'app',
  components: {
    sourceSelection,
    newsList
  },
    data() {
      return {
          source: ""
      }
    },
    methods: {
      sourceChanged: function (source) {
          this.source = source;
      }
    }
}
</script>

<style>
#app {
    background-color: white;
    padding: 20px;
}
</style>
