<template>
  <h1 class="reaction">Reaction time - {{ score }} ms</h1>
  <p class="rank">{{ rank }}</p>
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
            if (this.score < 250) {
                this.rank = 'Ninja Fingers'
            } else if (this.score < 400) {
                this.rank = 'Rapid Reflexes'
            } else {
                this.rank = 'Snail pace...'
            }
        }
    }
</script>

<style>
    .reaction {
        background: #0faf87;
        color: white;
    }
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>