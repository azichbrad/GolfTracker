<template>
  <div class="container">
    <form class="formLeague">
        <h3>Select a league to join: </h3><br><br>
        <label class="leagues">League you want to join:</label>
        <select name="leagues" v-model="newJoin.leagueId"  id="leagues">
            <option v-for="league in League"
            v-bind:key="league" v-bind:value="league.leagueId">{{league.leagueName}}
            </option>
            </select><br><br>
        <button class="btnbtn-submit" v-on:click="joinLeague">Join League</button>  <br>
    </form>   
  </div>
</template>

<script>
import authService from '@/services/AuthService.js';

export default {
    name: 'League',
    components:
    {
        
    },

data(){
    return{
        League: [],
        leagueId: '',
        leagueName: '',
        leagueAdmin: '',
        courseId: '',
        startDate: '',
        endDate: '',
        scoreLeague: '',
        newJoin: {
            leagueId: '',
            userId: this.$store.state.user.userId
    },
    }
},
created(){

     authService.Leagues().then((response) => {
              this.League = response.data;
          })
},
methods:{
joinLeague() {
      authService.joinLeague(this.newJoin).then(response=>{
             alert("You have joined this league successfully!")
            }
        ).catch(error => {alert("Error")})
    }  
}

}
</script>
