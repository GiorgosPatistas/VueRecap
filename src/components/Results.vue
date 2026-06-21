<template>
    <p>Reaction time - {{ score }} ms</p>
    <p class="rank"> {{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250){
            this.rank = 'God hands'
        } else if (this.score < 400) {
            this.rank = 'Rapid Reflaxes'
        } else {
            this.rank = 'Dogshit :('
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4rem;
        color: darkgoldenrod;
        font-weight: bold;
    }

</style>