<script>
import axios from 'axios';
const link = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=200';

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import { store } from './data/store.js';

export default {
    created() {
        axios.get(link).then(res => {
            store.cards = res.data.docs
        })
    },
    components: { AppHeader, AppMain }
}
</script>

<template>
    <!-- header -->
    <AppHeader />

    <!-- main -->
    <AppMain />
</template>

<style lang="scss">
@use 'assets/scss/style.scss';

body {
    background-color: var(--light-grey);
}
</style>