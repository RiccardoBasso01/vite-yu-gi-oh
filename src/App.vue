<script>
import axios from 'axios';
const link = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=200';

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import { store } from './data/store.js';

export default {
    data() {
        return {
            typeFilter: ''
        }
    },
    components: { AppHeader, AppMain },
    methods: {
        pokemonList(url) {
            axios.get(url).then(res => {
                store.cards = res.data.docs
            })
        },
        onTypeChange(type) {
            this.typeFilter = type
            const filteredLink = `${link}&eq[type1]=${type}`
            this.pokemonList(filteredLink)
        }
    },
    created() {
        this.pokemonList(link)
    }
}
</script>

<template>
    <!-- header -->
    <AppHeader @type-change="onTypeChange" />

    <!-- main -->
    <AppMain />
</template>

<style lang="scss">
@use 'assets/scss/style.scss';

body {
    background-color: var(--light-grey);
}
</style>