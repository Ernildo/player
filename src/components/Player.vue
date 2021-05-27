<template>
  <div class="player-container">
    <div class="area-filters"></div>
    <div 
      class="area-video" 
      @mouseover="over"
      @mouseout="out">
        <Video/>
        <Controls v-show="exibe"/>
      </div>
  </div>
</template>

<script>
import Video from './Video'
import Controls from './Controls'

export default {
  name: 'Player',

  components: {
    Controls,
    Video
  },

  data() {
    return {
      exibe: false
    }
  },

  methods: {
    over() {
      console.log('entrou aqui');
      this.exibe = true;
    },

    out() {
      console.log('saiu daqui');
      this.exibe = false;
    }
  }
}
</script>

<style scoped>
.player-container {
  height: 80%;
  width: 70%;
  background-color: white;
  border-radius: 8px;
  box-shadow: 0px 0px 20px 0px rgba(0, 0, 0, 0.50);

  display: grid;
  grid-template-rows: 100%;
  grid-template-columns: 10% 90%;
  grid-template-areas: "area-filters area-video";
}

.area-filters {
  grid-area: area-filters;
  height: 100%;
  width: 100%;
  background-color: transparent;
}

.area-video {
  grid-area: area-video;
  height: 100%;
  width: 100%;
  background-color: black;
  border-radius: 0 8px 8px 0;
}

</style>