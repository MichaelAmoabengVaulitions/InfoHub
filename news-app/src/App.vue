<template>
  <div class="container" id="app">
    <!--main components-->
    <sourceSelection></sourceSelection>
    <newsList></newsList>
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
    }
}
</script>

<style>
#app {

}
</style>
