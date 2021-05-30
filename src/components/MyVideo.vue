<template>
  <div class="video-container">
    <video ref="videoTag">
      <source :src="midia" type="video/mp4"/>
    </video>
  </div>
</template>

<script>
import midia from '../assets/teste.mp4'

export default {
  name: 'MyVideo',
 
  data() {
    return {
      midia
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