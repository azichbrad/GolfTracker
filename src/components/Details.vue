<template>
  <div>
      <h1>League Info</h1>
      <h2>League Name: {{League.leagueName}}</h2>
      <h2></h2>
      <h3>League Admin: {{League.leagueAdmin}}</h3>
      <h3></h3>
      <h3>What Course ID Is Being Played: {{League.courseId}}</h3>
    <h3></h3>
    <h3>Start Date: {{League.startDate}}</h3>
    <h3></h3>
    <h3>End Date:{{League.endDate}}</h3>
    <h3></h3>
    <h3>Description: {{League.description}}</h3>
    <h3></h3>

  </div>
</template>

<script>
import authService from '@/services/AuthService.js'

export default {
    data(){
        return{
<<<<<<< HEAD
            LeagueInfo:{
                leagueId: '',
                leagueName: '',
                leagueAdmin: '',
                courseId: '',
                startDate: '',
                endDate: '',
                scoreLeague: ''
            }
        }
    },
    created()
    {
        authService.getLeagueByLeagueId(this.leagueId).then((response) => {
              this.LeagueInfo = response.data;
    })
=======
            League: [],
            leagueId: '',
            leagueName: '',
            leagueAdmin: '',
            courseId: '',
            startDate: '',
            endDate: '',
            scoreLeague: '',
            description: '',

            // LeagueInfo:{
            //     leagueId: '',
            //     leagueName: '',
            //     leagueAdmin: '',
            //     courseId: '',
            //     startDate: '',
            //     endDate: '',
            //     scoreLeague: '',
            //     description: ''
            // }
        }
    },
    created(){
        authService.getLeagueByLeagueID(this.$route.params.leagueId).then((response) => {
              this.League = response.data;
          })
>>>>>>> a4816582a65cce1dcf17437d7fc3539008cfba9a
    }
    
}
</script>

<style>

</style>