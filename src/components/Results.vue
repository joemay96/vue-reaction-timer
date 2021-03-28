<template>
    <p>Reaction time - {{score}} ms</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: [
        "score"
    ],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 250){
            this.rank = "Ninja Fingers 🚀"
        } else if(this.score < 500) {
            this.rank = "Rapid Reflexes 🏎️"
        } else if(this.score < 1000) {
            this.rank = "You are quite fast! 🏃‍♂️"
        }else if(this.score < 1500) {
            this.rank = "Okey, nearly their 🚶‍♂️"
        }else {
            this.rank = "🐌 pace..."
        }
    }
}
</script>

<style>
.rank {
    font-size: 1.4rem;
    color: #0faf87;
    font-weight: bold;
}
</style>
