<template>
  <button 
    ref="playPause"
    @click="() => status = !status"></button>
</template>

<script>
export default {
  name: 'ButtonPlayPause',
  data() {
    return {
      status: false
    }
  },
  watch: {
    status(value) {
      const button = this.$refs.playPause;
      value ? button.classList.add('play') : button.classList.remove('play'); 
      this.$emit('click', value);
    }
  }
}
</script>

<style scoped>
button {
  height: 100px;
  width: 100px;
  cursor: pointer;
  background-color: transparent;
  background-image: url("../assets/button_pause.png");
}

.play {
  background-image: url("../assets/button_play.png");
}
</style>