<template>
  <div id="app">

    <div class="head-container">
      <vue-video-background :source="videoSource" :options="videoOptions"></vue-video-background>
    </div>

    <div class="container">

      <div class="title">
        <div class="d-inline-block logo">
          <img width="64" height="64" src="./assets/logo.png">
        </div>

        <div class="d-inline-block">
          <h1>VueJs Video Background</h1>
          <p class="lead">Display any video as background with many options.</p>
        </div>
      </div>

      <div class="content">
        <p>It's super simple to use and it has many functions</p>
        <p>Press <b>space</b> to pause the video.</p>
        <div class="buttons">
          <a class="btn btn-primary">Get it</a>
          <a class="btn btn-default">Docs</a>
        </div>
      </div>

    </div>

  </div>
</template>

<script>
import VueVideoBackground from '../../src/main.vue'
export default {
  name: 'app',
  data() {
    return {
      msg: 'Vue Video Backgroundp',
      videoSource: {
        mp4: 'https://ak8.picdn.net/shutterstock/videos/7726558/preview/stock-footage-floating-lanterns-in-yee-peng-festival-loy-krathong-celebration-in-chiangmai-thailand-uprisen-wid.mp4'
      },
      videoOptions: {
        autoplay: true,
        controls: false,
        muted: false,
        loop: true
      }
    }
  },
  components: {
    VueVideoBackground
  }
}
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.head-container {
  position: relative;
  width: 100%;
  height: 350px;
  border-bottom: 1px solid black;
}

.container {
  max-width: 90%;
  margin: 0 auto;
  text-align: center;
}

.d-inline-block {
  display: inline-block;
  line-height: 38px;
}

h1 {
  margin: 0;
  font-size: 42px;
}

b, strong {
  color: #42b983;
}

.title {
  margin: 20px 0;
}

p.lead {
  margin: 0;
  font-size: 20px;
}

.content p {
  margin: 8px;
}

.content .btn {
  text-transform: uppercase;
  background-color: #42b983;
  padding: 12px 16px;
  color: white;
  display: inline-block;
}

.content .buttons {
  margin-top: 20px;
}
</style>
