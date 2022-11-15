<template>
    <main>
        <div class="bianco">
            <div class="bluscuro">
                Found 62 characters
            </div>
            <div class="card bluscuro" v-for="character in data.return">
                {{ character }}
                <div class="grigio" v-for="name in data.return">
                    {{ name }}
                </div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'MainComponent',
    data() {
        return {
            apiURL: 'https://www.breakingbadapi.com/api/characters',
            character: [],
            name: []
        }
    },
    methods: {
        getApi() {
            axios.get(this.apiURL).then(
                (res) => {
                    this.MainComponent = [...res.data.results];
                    console.log(this.MainComponent);
                }
            )
        },
        created() {
            this.getApi();
        }
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