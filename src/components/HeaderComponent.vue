<template>
    <nav>
        <!-- icona -->
        <div>
            <h1>Breaking Bad Api</h1>
        </div>
        <div><button>Select category</button></div>
    </nav>

</template>

<script>
import MainComponent from './MainComponent.vue';

export default {
    name: "HeaderComponent",
    components: { MainComponent }
}

</script>

<style lang="scss" scoped>
@use '../assets/style/variables.scss' as *;
@use '../assets/style/general.scss' as*;

nav {
    height: 120px;
    width: 100%;
    color: white;
}
</style>