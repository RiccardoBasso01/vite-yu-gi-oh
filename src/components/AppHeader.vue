<script>
export default {
    data() {
        return {
            selectedType: undefined,
            types: [
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water"
            ]
        };
    },
}
</script>

<template>
    <header>
        <div class="title">
            <h1>POKÈDEX</h1>
            <img src="/icon.png" alt="">
        </div>
    </header>

    <div class="navbar-header">
        Seleziona Pokemon per tipo:
        <select v-model="this.selectedType">
            <option selected>Nessun Tipo</option>
            <option v-for="(type) in types" :key="type" :value="type">{{ type }}</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/style.scss';

header {
    background-color: rgb(9, 9, 85);
    height: 100px;
}

.navbar-header {
    position: sticky;
    top: 0;
    left: 0;
    background: linear-gradient(90deg, rgba(2, 0, 36, 1) 0%, rgba(9, 9, 121, 1) 35%, rgba(0, 212, 255, 1) 100%);
    color: white;
    text-align: center;
}

h1 {
    background-color: var(--light-grey);
    color: var(--dark-grey);
    padding: 10px;
    border-radius: 20px;
    border: 1px solid var(--dark-grey);
}

.title {
    display: flex;
    align-items: center;

    gap: 10px;
    justify-content: center;
}

img {
    width: 50px;
}
</style>