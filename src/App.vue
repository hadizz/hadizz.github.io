<template>
  <Header />
  <Bio v-bind:bio="data.bio" />
</template>

<script>
import Header from './components/Header';
import Bio from './components/Bio';
import data from './data';

export default {
  name: 'App',
  components: {
    Header,
    Bio,
  },
  data() {
    return {
      data: data,
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300;1,400;1,500&display=swap');

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

html {
  width: 70%;
  margin: 2rem auto;
}

#app {
  font-family: 'DM Mono', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  background-color: white;
  border-radius: 15px;
  border: 1px solid rgb(245, 245, 245);
  box-shadow: rgba(0, 0, 0, 0.1) 0px 2px 4px 0px;
}

@media screen and (max-width: 590px) {
  html {
    width: 90%;
  }
}
</style>
