<template>
    <button>Select category</button>
    <div class="bianco">
        <div class="bluscuro">
            Found 62 characters
        </div>
        <div class="card">
            <!--  : {{ }} -->
        </div>
    </div>

</template>

<script>
export default {
    name: 'MainComponent';
    data() {
        return {
            character: [],
        }
    }
},
methods: {
    insApi(){
        axios.ins('https://www.breakingbadapi.com/api/characters').then((res) => {
            console.log(res.data)
            this.character = [...res.data]
        })
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/variables.scss' as *;

.bluscuro {
    background-color: $bluscuro;
}
</style>