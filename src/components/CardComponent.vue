<template>
  <div class="card text-center bg-transparent">
      <img class="rounded-circle img-fluid" :src="item.image" alt="item.name">
      <h4 class="name">{{item.name}}</h4>
      <div>{{item.origin}}</div>
      <div class="specie">{{item.species}}</div>
            <!-- id {{item.id}} - name {{item.name}} - stato {{item.status}} - type {{item.type}} - species{{item.species}}  -->
  </div>
</template>

<script>
export default {
    name:'CardComponent',
    props:{
        item:Object
    }
}
</script>
<style lang="scss" scoped>
.card{
    border: none;
    padding: 10px;
    .name{
        padding: 3px;
    }
    img{
            box-shadow: 0 0 6px 3px rgba(#000, 0.15);
        }
    h4{
        text-transform: uppercase;
        font-size: 0.9em;
        &:after{
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            margin: 0.5rem auto;
            background: currentColor;
        }
        
    }
    .specie{
        font-weight: bold;
    }
}

</style>