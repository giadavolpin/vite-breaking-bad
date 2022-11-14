<template>
    <nav>
        <!-- icona -->
        <h1>Breaking Bad Api</h1>
        <button>Select category</button>
    </nav>
</template>

<script>
export default {
    name: "HeaderComponent"
}

</script>

<style lang="scss" scoped>
@use '../assets/style/variables.scss' as *;

nav {
    height: 120px;
    width: 100%;
    background-color: $blucard;
    color: white;
}
</style>