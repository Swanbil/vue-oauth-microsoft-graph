<template>
  <div>
    <base-header />
    <HomePage />
    <base-footer id="footer"/>
  </div>
</template>

<script>
import HomePage from './pages/HomePage.vue';
import BaseHeader from './components/BaseHeader.vue';
import BaseFooter from './components/BaseFooter.vue';

export default {
  name: 'App',
  components: {
    HomePage,
    'base-header': BaseHeader,
    'base-footer' : BaseFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  
}
</style>