<template>
  <div id="app">
    <number/>
  </div>
</template>

<script>
import number from './components/number.vue'

export default {
  name: 'app',
  components: {
    number
  }
}
</script>

<style>
html,body{
  margin: 0;
  padding: 0
}
*{
  color:#2EB738;
  box-sizing: border-box
}
#app{
  width: 1280px;
  margin: 30px auto;
  background: #F0F0F0;
  padding: 60px 70px;
  height: 1372px;
}
</style>
