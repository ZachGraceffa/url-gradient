<template>
  <div id="app" v-bind:style="gradient" />
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      showHowTo: !window.location.pathname,
      gradientSteps: window.location.pathname.split('/').filter(x => x)
    };
  },
  computed: {
    gradient() {
      console.log(window.location.pathname);
      return 'background-image : linear-gradient(to bottom right, #' + Array.prototype.join.call(this.gradientSteps, ', #') + ');';
    }
  }
}
</script>

<style>
html, body {
  height: 100%;
  margin: 0;
}

#app {
  height: 100%;
}
</style>
