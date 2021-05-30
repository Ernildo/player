<template>
  <Player/>
</template>

<script>
import Player from './components/Player.vue'

export default {
  name: 'App',
  components: {
    Player
  }
}
</script>

<style>
* {
  padding: 0;
  border: 0;
  margin: 0;
  box-sizing: border-box;
  vertical-align: baseline;
  list-style: none;
}

body {
  background-color: #1e272e;
}

</style>