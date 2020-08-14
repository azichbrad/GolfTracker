<template>
<div>
 
    <table class = "table">
      <tr>
        <th>League: </th>
        <th
        v-for="league in League"
        v-bind:key="league">{{league.leagueName}}</th>
      </tr>
      <tr>
         <th>User: </th>
        <th v-for="league in League"
        v-bind:key="league">{{$store.state.user.username}}</th>
      </tr>
      <tr>
        
        <th>Week: </th>
        <th
        v-for="leaderboard in Leaderboard"
        v-bind:key="leaderboard">{{leaderboard.week}}</th>
      </tr>
      <tr>
        <th>Score: </th>
        <th
        v-for="leaderboard in Leaderboard"
        v-bind:key="leaderboard">{{leaderboard.totalScore}}</th>
      </tr>
      

</table>
    </div>
</template>

<script>
import authService from '@/services/AuthService.js'

export default {
    data()
   {
     return {
       Leaderboard: [],
       week: '',
       totalScore: '',
       leagueId: '',
       userId: '',
        
         League: [],
             leagueName: '',
             leagueAdmin: '',
             courseId: '',
             startDate: '',
             endDate: '',
            scoreLeague: '',
            Users: [],
              username: '',
              passwordHash: '',
              salt: '',
              userRole: ''
   }
     },
     created(){
       authService.getLeaderboard().then((response) => {
              this.Leaderboard = response.data;
     }),
     authService.Leagues().then((response) => {
              this.League = response.data;
          }),
          authService.getUser(this.$route.params.id).then((response) => {
              this.Users = response.data;
          });   
              
     }
      
      
}
</script>
<style>
.table{
  padding: 20px;
}
.leaguename{
  display:grid;
  justify-content: space-between;
}
</style>