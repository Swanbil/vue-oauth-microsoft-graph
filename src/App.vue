<template>
  <div>
    <base-layout id="bl">
      <template v-slot:home>
        <HomePage />
      </template>
    </base-layout >
  </div>
</template>

<script>
import HomePage from './pages/HomePage.vue';
//import BaseHeader from './components/BaseHeader.vue';
//import BaseFooter from './components/BaseFooter.vue';
import BaseLayout from './components/BaseLayout.vue';

export default {
  name: 'App',
  components: {
    HomePage,
    //'base-header': BaseHeader,
    //'base-footer' : BaseFooter,
    'base-layout' : BaseLayout
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

</style>