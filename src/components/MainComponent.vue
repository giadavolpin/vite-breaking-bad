<template>
    <button>Select category</button>
    <div class="bianco">
        <div class="bluscuro">
            Found 62 characters
        </div>
        <div class="card">

        </div>
    </div>

</template>

<script>
export default {
    name: 'MainComponent',
    data() {
        return {
            apiURL: 'https://www.breakingbadapi.com/api/characters',
            character: []
        }
    }
};
methods: {
    getApi(){
        axios.get(this.apiURL).then(
            (res) => {
                this.MainComponent = [...res.data.results];
                console.log(this.MainComponent)
            }
        )
    },
    created(){
        this.getApi()
    }
}

</script>

<style lang="scss" scoped>
@use '../assets/style/variables.scss' as *;

.bluscuro {
    background-color: $bluscuro;
    color: white;
}
</style>