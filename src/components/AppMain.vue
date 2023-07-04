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
    padding: 50px 0;
}
</style>
