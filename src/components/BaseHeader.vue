<template>
  <div class="header bg-success d-flex flex-row" >
    <h3 class="p-2">
        <base-button :disable="false">
          <b-icon icon="house-fill" aria-hidden="true"></b-icon>
          Home
        </base-button>
    </h3>
    <h3 class="ms-auto p-2">
      <base-button :disable="true">
        <b-icon icon="person-circle" aria-hidden="true"></b-icon>
        Username
      </base-button>
    </h3>
    <base-button/>
    
  </div>
</template>

<script>
import BaseButton from './BaseButton.vue'
export default {
  name: 'BaseHeader',
  components: {
    'base-button' : BaseButton
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>