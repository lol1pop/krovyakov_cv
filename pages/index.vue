<template>
  <div class="layout">
    <Main/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Main from '~/components/Main.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Main
  }
})
</script>

<style lang="scss">
@import 'assets/css/colors';
.layout {
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  height: 1800px; /*TODO: replace 100%*/
  background-color: $dark-background;
}
</style>