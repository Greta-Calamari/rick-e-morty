<template>
<section class="container">
    <div class="row">
        <div class="col-6 col-md-4 col-lg-3 gy-0" v-for="character in filteredList" :key="character.id" >
        <card-component :item="character"/>
        </div>
        <div class="col-12 mb-5">
            <result-message :number="filteredList.length"/>
        </div>
    </div>
    <loader-component v-if="loading"/>
    <footer>
        <footer-component :len="filteredList.length" v-if="!loading"/>
    </footer>
</section>
</template>

<script>
import store from '../store.js';
import axios from 'axios';
import LoaderComponent from './LoaderComponent.vue'
import CardComponent from './CardComponent.vue';
import FooterComponent from './FooterComponent.vue';
export default {
    name:'MainGrid',
    components:{
        LoaderComponent,
        CardComponent,
        FooterComponent,
    },
    data(){
        return{
            apiPath:'https://api.sampleapis.com/rickandmorty/',
            characterList:[],
            loading:false,
            species:[]
        }
    },
    computed:{
        searchText(){
            return store.state.searchText;
        },
        filteredList(){
            if(this.searchText === ''){
                return this.characterList
            }
            return this.characterList.filter((item)=>{
                return item.species === this.searchText;
            });
        }
    },
    created(){
        this.loading = true;
        axios.get(this.apiPath +'characters').then((res)=>{
            this.characterList = [...res.data]
            this.characterList.forEach((el)=>{
                if(!this.species.includes(el.species)){
                    this.species.push(el.species)
                }
            });
            store.setSpecies(this.species);
            this.loading = false;
            console.log(this.characterList)
        }).catch((error)=>{
            console.log(error)
            this.loading = false;
        })
    }
}
</script>

<style lang="scss" scoped>

</style>
// gender: "Male"
// id: 1
// image: "https://rickandmortyapi.com/api/character/avatar/1.jpeg"
// name: "Rick Sanchez"
// origin: "Earth (C-137)"
// species: "Human"
// status: "Alive"
// type: "Human"