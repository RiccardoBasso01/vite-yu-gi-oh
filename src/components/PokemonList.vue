<script>
import { store } from '../data/store.js'

export default {
    data() {
        return { store };
    },

}
</script>

<template>
    <div class="container-s">

        <section id="card-list">
            <div class="card" v-for="card in store.cards">
                <div class="card-img">
                    <a href="#">
                        <img :src="card.imageUrl" :alt="card.name">
                    </a>
                </div>
                <div class="card-description">
                    <div class="card-subtitle">N° {{ card.number }}</div>
                    <h4>{{ card.name }}</h4>
                    <div class="pill">{{ card.type1 }}</div>
                    <div v-if="card.type2" class="pill">{{ card.type2 }}</div>
                </div>
            </div>

        </section>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/style.scss';

$numberOfCols: 2;
$spacing: 10px;



// cols

.card {
    width: calc(100% / $numberOfCols);
    padding: 0 $spacing;
    margin: $spacing 0;
    text-align: center;
    border-radius: 0;
    border: none;
    flex-direction: column;
}

// row
#card-list {
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    border: 1px solid var(--dark-grey);
    border-radius: 20px;

    margin: 0 - $spacing;
    margin: - $spacing 0;
}

a {
    display: block;
    height: 100%;
}

.card-img {
    overflow: hidden;
    height: 120px;

    img {
        height: 100%;
        object-fit: contain;
    }
}

.card-description {
    text-align: start;
    padding-left: 30px;
}

.card-subtitle {
    font-size: var(--font-size-s);
    color: var(--grey);
    margin-bottom: 10px;
}

.pill {
    font-size: var(--font-size-xs);
    display: inline-block;
    padding: 5px;
    margin-top: 10px;
    border: 1px solid var(--dark-grey);
    border-radius: 20px;
    margin-right: 10px;
}

@media screen and (min-width: 768px) {
    $numberOfCols: 3;

    .card {
        width: calc(100% / $numberOfCols);
    }
}

@media screen and (min-width: 992px) {
    $numberOfCols: 4;

    .card {
        width: calc(100% / $numberOfCols);
    }
}
</style>
