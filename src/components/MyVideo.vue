<template>
  <div class="video-container">
    <video ref="videoTag">
      <source 
        :src="midia" 
        type="video/mp4"
        crossOrigin/>
    </video>
  </div>
</template>

<script>
import midia from '../assets/teste.mp4'

export default {
  name: 'MyVideo',
  
  props: {
    playPause: {
      type: Boolean,
      default: false
    }
  }, 

  data() {
    return {
      midia
    }
  },

  watch: {
    playPause(val) {
      const video = this.$refs.videoTag;
      val ? video.play() : video.pause();
    }
  }
}
</script>

<style scoped>
.video-container {
  height: 100%;
  width: 100%;
  
  position: relative;
  float: left;

  display: flex;
  justify-content: center;
  align-items: center;
}

  .video-container video {
    height: 99%;
    width: 99%;
  }
</style>