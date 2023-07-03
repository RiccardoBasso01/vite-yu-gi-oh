<script>
export default {
    data() {
        return {

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
</template>

<style lang="scss" scoped>
@use '../assets/scss/style.scss';

header {
    background-color: rgb(9, 9, 85);
    height: 100px;
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