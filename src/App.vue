<template>
<div class="container-fluid mt-3" style="background: #232323; margin: 0;	font-family: Montserrat, Avenir">
    <div class="jumbotron">

      <Header />

    </div>
  </div>
</template>

<script>

import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
#jumbotron {
  color: #2c3e50
}
</style>
