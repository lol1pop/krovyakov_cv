<template>
  <main class="container">
    <section>
      <Header/>
      <Intro/>
    </section>
  </main>
</template>

<script>
import Intro from '~/components/Intro';
import Header from '~/components/Header';

export default {
  name: 'Main',
  components: {
    Intro,
    Header
  }
}
</script>

<style scoped lang="scss">
@import "assets/css/colors";
@import "assets/css/mixin";
main {
  background-color: $dark;
  @include box-shadow(0px 0px 30px 0px $D-dark-purple);
  min-height: 1360px; /*TODO: replace 100%*/
  padding: 0;
}
</style>