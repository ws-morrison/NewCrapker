<template>
  <div id='app'>
    <HeaderStart/>
    <BuCalc/>
  </div>
</template>

<script>
import HeaderStart from './components/HeaderStart'
import BuCalc from './components/BuCalc'

export default {
  name: 'App',
  components: {
    HeaderStart,
    BuCalc
  }
}
</script>

<style scoped>
#app {
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
