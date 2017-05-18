<template>
  <div id="app">
    <list-view></list-view>
    <player-view></player-view>
  </div>
</template>

<script>
import ListView from './components/ListView'
import PlayerView from './components/PlayerView'

export default {
  name: 'app',
  components: {
    ListView,
    PlayerView
  }
}
</script>

<style lang="scss" scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  width: 800px;
  height: 480px;
  margin: auto;
  background-color: #fff;
  box-shadow: 0 0 5px rgba(0,0,0,.3);
}
</style>
