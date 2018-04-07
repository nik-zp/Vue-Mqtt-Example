<template>
  <div id="app">
    <img src="./assets/logo.png">
    <publish></publish>
    <sub1></sub1>
    <sub2></sub2>
    <sub3></sub3>
  </div>
</template>

<script>
import Publish from './components/Publish'
import Sub1 from './components/Sub1'
import Sub2 from './components/Sub2'
import Sub3 from './components/Sub3'
export default {
  name: 'app',
  components: {
    Publish, Sub1, Sub2, Sub3
  },
  mounted () {
    this.$mqtt.subscribe('VueMqtt/#')
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.sub {
  width: 31%;
  float: left;
  border: 1px solid #ccc;
  margin: 20px 1%;
  padding: 20px 0;
}
button {
  padding: 10px 20px;
}
</style>
