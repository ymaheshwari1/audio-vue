<template>
  <div v-show="display">
    <div id="modal">
      <div id="close" @click="close"></div>
      <div id="content">
        <div id="title">{{ title }}</div>
        <audio controls id="audio-player">
          <source id="audio-source" src="../assets/audio.mp3" type="audio/mpeg" />
        </audio>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  data () {
    return {
      display: false,
      title: '',
      image: ''
    }
  },
  methods: {
    show: function (title, image) {
      this.display = true
      this.title = title
      this.image = image
      document.body.style.overflow = 'hidden'
    },
    close: function () {
      this.display = false
      document.getElementById('audio-player').pause()
      document.getElementById('audio-player').currentTime = 0
      document.body.style.overflow = 'auto'
    }
  }
}
</script>

<style scoped>
#modal {
  background: grey;
  background-image: url("../assets/logo.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: 1;
}
#close {
  cursor: pointer;
  position: absolute;
  top: 0;
  right: 0;
  height: 30px;
  width: 30px;
  background-image: url("../assets/close.svg");
}
#content {
  width: 100%;
  position: absolute;
  bottom: 0;
  text-align: center;
  font-size: 36px;
}
#audio-player {
  width: 100%;
  filter: sepia(20%) saturate(70%) grayscale(1) contrast(99%) invert(12%);
}
</style>
