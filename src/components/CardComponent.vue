<template>
<!-- {
        "id": 1,
        "name": "Rick Sanchez",
        "status": "Alive",
        "species": "Human",
        "type": "Human",
        "gender": "Male",
        "origin": "Earth (C-137)",
        "image": "https://rickandmortyapi.com/api/character/avatar/1.jpeg"
    }, -->
<div class="text-center">
    <img class="img-fluid" :src="item.image" alt="item.name">
    <h4 class="mt-3">{{item.name}}</h4>
    <div>{{item.origin}}</div>
    <div class="fw-bold">{{item.type}}</div>
</div>
  
</template>

<script>

export default {
    name:'CardComponent',
    props:{
        item: Object
    }
}
</script>

<style  lang="scss" scoped>
@import '../style/vars.scss';

h4{
    text-transform: uppercase;
    &:after{
        content: '';
        display: block;
        width: 50px;
        height: 2px;
        margin: 1rem auto;
        background-color: currentColor;
    }
}
img{
    border-radius: 50%;
    box-shadow: 0 0 6px 3px rgba(#000, 0.15); 
}

</style>