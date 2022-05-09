<template>
<div>
    <div class="input-group">
  <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username with two button addons" v-model="inputText" @keyup.enter="search">
  <button class="btn btn-outline-secondary" type="button" @click="search">Button</button>
  <button class="btn btn-outline-secondary" type="button" @click="reset">reset</button>
</div>
</div>
    
</template>
<script>
export default {
    name:'SearchBar',
    data(){
        return{
            inputText:'',
        }
    },methods:{
        search(){
            console.log(this.inputText)
            
        },
        reset(){
            this.inputText=''
        },
    }
}
</script>