<template>
    <main>
        <div class="bianco">
            <div class="bluscuro">
                Found 62 characters
            </div>
            <div class="card bluscuro" v-for="character in characters">
                <img :src="character.img" alt="" />
                <div class="grigio">
                    {{ character.name }}
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios';

export default {
    name: 'MainComponent',
    data() {
        return {
            apiURL: 'https://www.breakingbadapi.com/api/characters',
            characters: [],

        }
    },
    methods: {
        getApi() {
            axios.get(this.apiURL).then(
                (res) => {

                    // res.data.results.forEach(element => {
                    //     this.character.push(element)
                    // });
                    this.characters = [...res.data];
                    console.log(this.characters);
                }
            )
        }
    },
    created() {
        this.getApi();
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/variables.scss' as *;
@use '../assets/style/general.scss' as*;

.bluscuro {
    background-color: $bluscuro;
    color: white;
}

.grigio {
    color: $grigio;
}

.bianco {
    background-color: white;
}
</style>