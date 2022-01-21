<template>
  <p>Reaction time - {{score}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
props: ['score'],
data(){
    return{
        rank:null
    }
},
mounted(){
    if(this.score < 250 ){
        this.rank ="You're a speedster"
    }else if (this.score < 400){
        this.rank = "You're  Fast"
    }else{
        this.rank = "You're slow"
    }
}
}
</script>

<style scoped>
.rank{
    color:red
}
</style>