<template>
  <div class="input-group mb-3 w-100">
    <select name="species" id="species" v-model="inputText" @change="changeSearch">
        <option value="">all</option>
        <option :value="specie" v-for="(specie,index) in characterSpecies" :key="index">{{specie}}</option>
    </select>
    <div class="input-group-append">
        <button class="btn btn-outline-secondary" type="button" @click="changeSearch">Search</button>
        <button class="btn btn-outline-secondary" type="button" @click="reset">Reset</button>
    </div>
</div>
</template>

<script>
import store from '../store.js'
export default {
    name:'SearchBar',
    data(){
        return{
            inputText:'',
        }
    },
    computed:{
        characterSpecies(){
            return store.state.speciesList 
        }
    },
    methods:{
        changeSearch(){
            store.setText(this.inputText);
        },
        reset(){
            this.inputText=''
            store.setText(this.inputText);
        }
    }
}
</script>

<style lang="scss">

</style>