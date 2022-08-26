<template>
    
    <div class="card">
        <div class="card-header">
            <img :src="character.image" alt="">
        </div>
        <div class="card-body">
            <h3>{{character.name}}</h3>
            <hr>
            <p>{{character.origin}}</p>
            <p>{{character.species}}</p>
        </div>
    </div>
</template>

<script>

export default {
    name: 'AppSingleCharacters',
    props:{
        character: Object
    }
}

</script>


<style scoped lang="scss">
.card-header{
    img{
        width: 100%;
    }
}
</style>