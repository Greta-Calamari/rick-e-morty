<template>
  <div id="app">
    <header-component :title = 'titolo'/>
    <main>
      <grid-component/>
    </main>
    <!-- <footer-component/> -->
  </div>
  
 
</template>

<script>

import GridComponent from './components/GridComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
// import FooterComponent from './components/FooterComponent.vue'


export default {
  name: 'App',
  components: {
    HeaderComponent,
    GridComponent,
    // FooterComponent
},
  data(){
    return{
      titolo: 'Rick & Morty',
    }
  }
}
</script>

<style lang="scss">
@import "./style/general.scss";


</style>
