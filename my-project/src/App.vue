<template>
  <div id="app">
    <header-view></header-view>
    <router-view/>
  </div>
</template>

<script>
import HeaderView from './components/HeaderView'
export default {
    components: {
      HeaderView
  }
}
</script>


<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50

#nav
  padding 30px
  a
    font-weight bold
    color #2c3e50
    &.router-link-exact-active
      color #42b983
</style>
