<template>
  <div id="app">
    <div v-bind:style="gradient">Hello World!</div>
  </div>
</template>

<script>
export default {
  name: 'App',
  computed: {
    gradient: function() {
      return "background-image : linear-gradient(to bottom right, red, yellow);";
    }
  }
}
</script>
