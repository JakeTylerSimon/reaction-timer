<template>
    <p>Reaction Time: {{score}} ms</p>
    <p class="rank">{{rank}}</p>
</template>

<script>
    export default {
        props: ['score',],
        data() {
            return {
                rank: null,
            }
        },
        mounted() {
            if(this.score < 350) {
                this.rank = 'Elite Status'
            } else if(this.score < 450) {
                this.rank = 'Quick with it'
            } else {
                this.rank = 'Come onnn, you can do better'
            }
        }
    }
</script>

<style>
    .rank {
        font-size: 1.4rem;
        color: teal;
        font-weight: bold;
    }
</style>