<template>
  <div class="result">
      <p>Your reaction time is : {{score}} ms</p>
      <p class="rank"> {{ rank }}</p>
  </div>
</template>

<script>
export default {
    props: ['score'],
    data(){
        return {
            rank: null,
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank = 'Well done Kijana'
        }else if( this.score < 500 ){
            this.rank = 'Rapid reflexes'
        }else{
            this.rank = 'Snail pace'
        }
    }
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>