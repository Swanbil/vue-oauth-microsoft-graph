<template>
  <div class="header bg-success d-flex flex-row" >
    <h3 class="p-2">
        <base-button :disable="false" :color="'success'">
          <b-icon icon="house-fill" aria-hidden="true"></b-icon>
          Home
        </base-button>
    </h3>
    <h3 class="ms-auto p-2">
      <async-button :disable="false" :color="'success'" >
        <b-icon icon="person-circle" aria-hidden="true"></b-icon>
        Username
      </async-button>
    </h3>
        
  </div>
</template>

<script>
import AsyncButtonVue from './AsyncButton.vue'
import BaseButton from './BaseButton.vue'

export default {
  name: 'BaseHeader',
  components: {
    'base-button' : BaseButton,
    'async-button' : AsyncButtonVue
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>