<template>
<div>
    <!-- @keyup.enter="search" -->
  <select type="text" v-model="inputText" @change="changeSearch" >
      <option :value="specie" v-for="specie in characterSpecies" :key="specie">{{specie}}</option>
      <option value="">all</option>
  </select>
  <button class="btn btn-outline-secondary" type="button" @click="search">Cerca</button>
  <button class="btn btn-outline-secondary" type="button" @click="reset">Reset</button>
<!-- <div class="input-group">
</div> -->
</div>
    
</template>
<script>
export default {
    name:'SearchBar',
    data(){
        return{
            inputText:'',
        }
    },props:['characterSpecies'],
    methods:{
        
        reset(){
            this.inputText='';
            this.$emit('mySearch',this.inputText)
        },
        search(){
            this.$emit('mySearch',this.inputText);
            this.inputText='';


        },
    }
}
</script>