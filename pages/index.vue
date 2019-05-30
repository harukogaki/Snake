<template>
  <div class="container">
    <div class="game-screen">
      <div class="game-title">
        Snake
      </div>
      <Box v-for="option in options" :key="option" class="box game-option">
        {{ option }}
      </Box>
    </div>
    <div class="demo-game"></div>
  </div>
</template>

<script>
import posed from 'vue-pose'
export default {
  components: {
    Box: posed.div({
      pressable: true,
      hoverable: true,
      init: { scale: 1 },
      press: { scale: 1.2 },
      hover: {
        scale: 1.1
      }
    })
  },
  data() {
    return {
      options: ['Play', 'Help']
    }
  }
}
</script>

<style scoped>
.container {
  padding: 16px;
  margin: 0;
  max-width: 100%;
  display: flex;
  flex-direction: column;
}
.game-title {
  font-size: 56pt;
  font-weight: bold;
  margin-bottom: 16pt;
}
.game-option {
  width: 50%;
  margin: 16pt 25%;
}
.game-screen {
  text-align: center;
  flex: 1;
}
.demo-game {
  flex: 1;
}
.box {
  background-color: palegoldenrod;
}
</style>
``