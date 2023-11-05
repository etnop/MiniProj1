<template>
  
    <ViewHome></ViewHome>
</template>

<script>
import ViewHome from './components/ViewHome.vue';

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap'
import '@fortawesome/fontawesome-free/css/all.css'

export default {
  name: 'App',
  components: {
    ViewHome
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
 margin: 0px;
 padding: 0px;
}

</style>
