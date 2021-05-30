<template>
  <div class="controls-container">
    <div class="name-area">
      <h1> Nome do meu vídeo </h1>
    </div>

    <div class="color-controls-area">
      <button 
        :key="index" 
        v-for="(btn, index) in buttons"
        :class="btn">
      </button>
    </div>
    
    <div class="play-pause-ara"></div>
    
    <div class="times-area"></div>
    
    <div class="controls-area"></div>
  </div>
</template>

<script>
export default {
  name: 'Controls',
  data() {
    return {
      buttons: ['colors', 'black-white', 'red', 'blue', 'green']
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
  /* background-color: red; */
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  padding-right: 20%;
}

  .color-controls-area button {
    height: 45px;
    width: 45px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px 2px rgba(rgb(87, 32, 32) 0.2);
    cursor: pointer;
  }

    .colors { background-image: linear-gradient(blue, red, green); }
    .black-white { background-image: linear-gradient(black, white); }
    .red { background-color: red; }
    .blue { background-color: blue; }
    .green { background-color: green; }

  .color-controls-area button:focus {
    border: 2px solid black;
  }

.play-pause-ara {
  grid-area: c;
  /* background-color: green; */
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