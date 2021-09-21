<template>
  <div class="button">
    <b-button v-if="!this.disable" :variant="this.color" @click="this.onClick">
        <slot></slot>
    </b-button>
    
    <b-button v-else :variant="this.color" disabled>
        <slot></slot>
    </b-button>

  </div>
</template>

<script>
export default {
  name: "BaseButton",
  props: ['disable','color','onClick']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>