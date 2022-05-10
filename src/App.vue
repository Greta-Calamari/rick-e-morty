<template>
  <div id="app">
    <header-component :intestazione="titolo"/>
    <main>
      <main-grid/>
    </main>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainGrid from './components/MainGrid.vue'
export default {
  name: 'App',
  data(){
    return{
      titolo:"Rick & Morty"
    }
  },
  components: {
    HeaderComponent,
    MainGrid,
  }
}
</script>

<style lang="scss">
@import './style/general.scss';
</style>
