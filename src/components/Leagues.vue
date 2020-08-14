<template>
    <div class = "leagues">
        <div class="league"
        v-for="league in League"
        v-bind:key="league">
    <router-link v-bind:to="{name:'leaguesByID'}">{{league.leagueName}}</router-link>
    </div>
    </div>
</template>

<script>
import authService from '@/services/AuthService.js'

export default {
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
            Users: [],
              userId: '',
              username: '',
              passwordHash: '',
              salt: '',
              userRole: ''
        }
    },
    created(){
          authService.getLeaguesByUserId(this.$store.state.user.username).then((response) => {
              this.League = response.data;
          })
          
    //   authService.Leagues().then((response) => {
    //            this.League = response.data;
    //        })
      
     }
}

</script>

<style>
.leagues{
    
  display: flex;
  justify-content: space-between;
  align-items: right;
    font-size: 35px;
    font-family: Arial, Helvetica, sans-serif;
    color: #88f29b;

}
</style>
