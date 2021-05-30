<template>
  <div 
    class="player-container"
    @mouseover="() => showControls = true"
    @mouseout="() => showControls = false">
    <!-- Serão substituidos por componentes -->
    <MyVideo/>
    <Controls v-show="showControls"/>
    <!-- <div class="video"></div> -->
    <!-- <div class="controls" v-show="showControls"></div> -->
  </div>
</template>

<script>
import MyVideo from './MyVideo.vue'
import Controls from './Controls.vue'

export default {
  name: 'Player',
  components: { 
    MyVideo,
    Controls
  },
  data() {
    return {
      showControls: false
    }
  }
}
</script>

<style scoped>
.player-container {
  height: 90%;
  width: 80%;
  box-shadow: 0px 0px 10px 2px rgba(0,0,0, 0.4);
  border-radius: 8px;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
}

</style>