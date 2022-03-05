<template>
  <header>
    <div class="container">
      <div class="menu-main">
        <div class="menu-main__logo"></div>
        <div class="menu-main__items"></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped lang="scss">
@import "assets/css/colors";
.menu-main {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  height: 75px;
}
.menu-main__logo {
  width: 75px;
  margin-left: 16px;
  margin-right: 16px;
}
.menu-main__items {
  box-sizing: border-box;
  border-bottom: solid $D-dark-gray 1px;
  margin-left: 16px;
  margin-right: 16px;
  
  flex-grow: 1;
  max-width: 100%;
  align-self: stretch;
}
</style>