//"https://api.sampleapis.com/rickandmorty/characters"
<template>
<section class="container">
    <SearchBar/>
    <loader-component v-if="loading"/>
        <div class="row">
            <div class="col-6 col-md-4 col-lg-3 gy-3" v-for="character in getFilteredList()" :key="character.id">
            <card-component :item="character"/>
            </div>
        </div>
  <footer-component :len="characterList.length"/>
</section>
</template>
<script>

import axios from 'axios';
import LoaderComponent from './LoaderComponent.vue';
import CardComponent from './CardComponent.vue';
import FooterComponent from './FooterComponent.vue';
import SearchBar from './SearchBar.vue';


export default {
    name: 'GridComponent',
    components: {
    LoaderComponent,
    CardComponent,
    FooterComponent,
    SearchBar,
},
    data(){
        return {
            characterList: [],
            filteredList:[],
            searchText:'',
            apiPath: 'https://api.sampleapis.com/rickandmorty/',
            loading: false
        }
    },methods:{
        getFilteredList(){
            this.filteredList = this.characterList.filter((el)=>el.name.toLowerCase().includes(this.searchText.toLoweCase()))
            console.log(this.filteredList)
        }

    },
    mounted() {
        this.loading = true;
        setTimeout(()=>{
            axios.get(this.apiPath + 'characters').then((res)=>{
            this.characterList = res.data;
            this.loading = false
            console.log(this.characterList)
        }).catch((error) => {
            console.log(error)
        }) 
        },1000)
    }    
 }

</script>

<style lang="scss" scoped>

</style>