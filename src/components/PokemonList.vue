<script>
import axios from 'axios';
const link = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?eq[type1]=Electric&sort[number]=desc';
export default {
    data() {
        return {
            cards: []
        };
    },
    created() {
        axios.get(link).then(res => {
            this.cards = res.data.docs
        })
    }
}
</script>

<template>
    <section id="card-list">
        <ul>
            <li v-for="card in this.cards">
                <a href="#">
                    <img :src="card.imageUrl" :alt="card.name">
                </a>
            </li>
        </ul>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/style.scss';

img {
    width: 50px;
}
</style>
