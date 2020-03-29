<template>
  <div id="app" v-bind:style="gradient" /> 
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
    gradientSteps: [ 'red', 'yellow'],
    gradientStr: Array.prototype.join.call(arguments, ',')
    };
  },
  computed: {
    gradient() {
      return 'background-image : linear-gradient(to bottom right, ' + Array.prototype.join.call(this.gradientSteps, ', ') + ');';
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
