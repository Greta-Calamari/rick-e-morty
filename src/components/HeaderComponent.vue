<template>
<header>
    <h1 class="text-center display-1 my-1">{{intestazione}}</h1>
    <div class="m-5">
            <search-bar/>
    </div>
</header>
</template>
<script>
import SearchBar from './SearchBar.vue';
export default {
   name:'HeaderComponent',
   components:{
       SearchBar,
   },
   props:['intestazione']
}
</script>
<style lang="scss">

</style>