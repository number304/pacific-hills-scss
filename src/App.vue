<template>
  <div id="app">
    <TheHeader />
    <TheLanding />
    <ApartmentList />
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import TheLanding from './components/TheLanding.vue'
import ApartmentList from './components/ApartmentList.vue'
import TheFooter from './components/TheFooter.vue'

export default {
  name: 'App',
  components: {
    TheHeader,
    TheLanding,
    ApartmentList,
    TheFooter
  }
}
</script>

<style lang="scss">
$background-color: #A9FFCB;

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  overflow-x: hidden;
}

#app {
  font-family: 'Avenir', Helvetica, 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgba($color: #000000, $alpha: 0.87);
}

.container {
  margin: 0 auto;
  padding: 30px 20px;

  &.colored {
    background-color: $background-color;
  }
}
</style>
