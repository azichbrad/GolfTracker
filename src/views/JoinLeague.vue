<template>
  <div class="joinLeague">
      <join-league/>
  </div>
</template>

<script>
import JoinLeague from '@/components/JoinLeague.vue'
export default {

    components:{
        JoinLeague
    }
}
</script>

<style>
.container{
    display: flex;
    justify-content: center;
}
.formLeague{
    display: flex;
    justify-content: center;
    width: 33%;
    font-family: 'Bree Serif';
    color: #2d487a;
    font-size: 30px; 
    background-color: whitesmoke;
    padding: 20px;
    margin: 10px;
    border: 6px solid;
    opacity: 0.9;
}
.leagues{
    color: #2d487a;
    font-size: 25px;
    font-family: 'Bree Serif';
    text-align: center;
}
.btnbtn-submit{
    display: block;
}

</style>