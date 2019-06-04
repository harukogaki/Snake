<template>
  <div class="container">
    <div class="game-screen">
      <div class="game-title">Snake</div>
      <Box
        class="button column is-primary is-large"
        style="margin-bottom: 16px;"
        >Play</Box
      >
      <Box class="button column is-primary is-large">Help</Box>
    </div>
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
  }
}
</script>

<style scoped>
.container {
  padding: 16pt;
  margin: 0;
  min-width: 100%;
  width: 50%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.game-title {
  font-size: 56pt;
  font-weight: bold;
  margin-bottom: 8pt;
}
.game-screen {
  width: 33%;
  text-align: center;
  align-items: center;
}
</style>
