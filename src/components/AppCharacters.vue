<template>
    <main class="container py-5">
        <div class="row d-flex flex-wrap">
            <AppSingleCharacters class="col-4" v-for="character in characters" :key="character.id" :character="character"/>
        </div>
    </main>
</template>

<script>
import axios from 'axios'
import AppSingleCharacters from './AppSingleCharacters.vue'

export default{
    name: 'AppCharacters',
    components:{
    AppSingleCharacters,
    },
    data(){
        return{
            characters: [],
            endpoint: 'https://api.sampleapis.com/rickandmorty/characters'
        }
    },
    created(){
        this.getApiData()
    },
    methods:{
        getApiData: function(){
            axios.get(this.endpoint)
            .then( response => {
                this.characters = response.data
            })
            .catch(err => {
                console.log(err)
            })
        }
    }
}
</script>

<style scoped lang="scss">

</style>