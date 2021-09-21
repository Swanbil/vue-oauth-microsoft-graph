<template>
  <div class="button">
    <b-button v-if="!this.disable" variant="success">
        <slot></slot>
    </b-button>
    
    <b-button v-else class ="disabled"  variant="success">
        <slot></slot>
    </b-button>

  </div>
</template>

<script>
export default {
  name: "BaseButton",
  props: ['disable']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.disabled{
    background-color:rgb(112, 112, 112);
}
</style>