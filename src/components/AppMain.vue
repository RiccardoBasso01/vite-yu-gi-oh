<script>
import PokemonList from './PokemonList.vue';


export default {
    data() {
        return {

        };
    },
    components: { PokemonList }

}
</script>

<template>
    <main>
        <PokemonList />
    </main>
</template>

<style lang="scss">
@use '../assets/scss/style.scss';

main {
    height: calc(100vh - 100px);
    padding: 50px 0;
    overflow: auto;
}
</style>
