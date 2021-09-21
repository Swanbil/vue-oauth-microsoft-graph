<template>
  <div>
    <base-header id="header"/>
      <slot name="home"></slot>
    <base-footer id="footer"/>
  </div>
</template>

<script>
import BaseFooter from './BaseFooter.vue';
import BaseHeader from './BaseHeader.vue';
export default {
  components: { BaseFooter, BaseHeader },
  name: "BaseLayout",
  'base-header': BaseHeader,
  'base-footer' : BaseFooter
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  
}
</style>