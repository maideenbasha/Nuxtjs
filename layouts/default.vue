<template>
    <div id ="app">
        <NavBar />
        <nuxt />
    </div>
  </template>

<script>
import NavBar from '~/components/NavBar.vue'

export default {
    components:{
        NavBar
    }       
}
</script>

<style>
#app {
  box-sizing: border-box;
  width: 500px;
  padding: 0 20px 20px;
  margin: 0 auto;
}
a {
  color: #39b982;
  font-weight: 600;
  background-color: transparent;
}
.error-message{
  color:red;
}

</style>