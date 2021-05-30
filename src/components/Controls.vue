<template>
  <div class="controls-container">
    <div class="name-area">
      <h1> Nome do meu vídeo </h1>
    </div>

    <div class="color-controls-area">
      <ButtonColors/>
    </div>
    
    <div class="play-pause-ara">
      <ButtonPlayPause/>
    </div>
    
    <div class="times-area">
      <ListTimes @click="teste"/>
    </div>
    
    <div class="controls-area"></div>
  </div>
</template>

<script>
import ButtonColors from './ButtonColors.vue'
import ButtonPlayPause from './ButtonPlayPause.vue'
import ListTimes from './ListTimes.vue'

export default {
  name: 'Controls',
  components: {
    ButtonColors,
    ButtonPlayPause,
    ListTimes
  },
  methods: {
    teste(time) {
      console.log(time)
    }
  }
}
</script>

<style scoped>
.controls-container {
  height: 100%;
  width: 100%;
  position: relative;
  top: -100%;
  background-color: rgba(0, 0, 0, 0.9);
  
  display: grid;
  grid-template-rows: 20% 50% 30%;
  grid-template-columns: 35% 30% 35%;
  grid-template-areas: 
    "a a a"
    "b c d"
    "e e e";
}

.name-area, .color-controls-area, .play-pause-ara, .times-area, .controls-area {
  height: 100%;
  width: 100%;
  display: flex;
}

.name-area {
  grid-area: a;
  /* background-color: blue; */
  padding: 0 5%;
  justify-content: flex-start;
  align-items: center;
}

  .name-area h1 {
    font-family: 'Roboto', sans-serif;
    font-weight: 400;
    color: white;
  }

.color-controls-area {
  grid-area: b;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  padding-left: 14%;
}

.play-pause-ara {
  grid-area: c;
  /* background-color: green; */
  display: flex;
  justify-content: center;
  align-items: center;
}

.times-area {
  grid-area: d;
  /* background-color: bisque; */
}

.controls-area {
  grid-area: e;
  /* background-color: brown; */
}
</style>