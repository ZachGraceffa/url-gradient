<template>
  <div id="app" v-bind:style="gradient">
    <div id="content">
      <img id="mom-pic" src="https://gdurl.com/fbqa" />
      <h1>Happy Mother's Day!</h1>
      <p>
        In every way<br />
        I wish I could train<br />
        To Robinwood Lane<br />
        Then I could seek<br />
        To kiss your cheek<br />
        But since we are in quarantine<br />
        Expect a gift on the 14th
      </p>
      <p>
        I love you,<br />
        Zach
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      gradientSteps: ["E25B6A", "dfddf1", "FFAEAA"]
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
  text-align: center;
}

#content {
  display: block;
  position: relative;
  top: 30%;
  left: 50%;
  max-height: 50%;
  max-width: 30%;
  transform: translate(-50%, -50%);
}

h1 {
  color : seashell;
  text-shadow: 2px 2px 5px red;
}

p {
  font-size: 150%;
  color: seashell;
  text-shadow: 2px 2px 5px red;
}

#mom-pic {
    height: 100%; 
    width: 100%; 
    object-fit: 'contain';
}

</style>
