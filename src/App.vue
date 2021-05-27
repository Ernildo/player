<template>
  <div class="app-container">
    <Player/>
  </div>
</template>

<script>
import Player from './components/Player'

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

.app-container {
  height: 100vh;
  width: 100%;
  background-color: #2f3640;
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>