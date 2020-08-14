<template>
 <div class="home">
    <div class="leaderboardDisplay"> 
    <h1 class = "myleagues">My Leagues</h1>
  <div class = "leaguecomponent"><Leagues/></div>
  </div>
  </div>
</template>

<script>
import Leagues from '@/components/Leagues.vue';

export default {
    name: 'League',
    components:
    {
        Leagues
    },
}
</script>

<style>
.myleagues{
  display: flex;
  justify-content: center;
  font-family: 'Bree Serif';
  color: white;
  background-color: #1b3869;
  opacity: 1.0;
  font-weight:bold;
  font-size: 45px;
}
.img {
  display: flex;
  justify-content: center;
}
.create{
  font-size: 35px;
  font-family: 'Bree Serif';
  display:flex;
  justify-content: left;
  border: groove;
  border-radius: 5px;
  float: left;
  width:33%;
  padding: 50px;
  background-color: whitesmoke;
  opacity: 0.85;
}
.scores{
  font-size: 35px;
  font-family: 'Bree Serif';
  display:flex;
  justify-content: left;
  border: groove;
  border-radius: 5px;
  float: left;
  width:33%;
  padding: 50px;
  background-color: whitesmoke;
  opacity: 0.85;

}
.leaderboard{
  font-size: 35px;
  font-family: 'Bree Serif';
  display:flex;
  justify-content: left;
  border: groove;
  border-radius: 5px;
  float: left;
  width:33%;
  padding: 50px;
  background-color: whitesmoke;
  opacity: 0.85;
}
.locate{
  font-size: 35px;
  font-family: 'Bree Serif';
  display:flex;
  justify-content: left;
  border-radius: 5px;
  float: left;
  width:20%;
  padding: 50px;
  background-color: whitesmoke;
  opacity: 0.85;
}
.addcourses{
  font-size: 35px;
  font-family: 'Bree Serif';
  display:flex;
  justify-content: left;
  border-radius: 5px;
  float: left;
  width:20%;
  padding: 50px;
  background-color: whitesmoke;
  opacity: 0.85;
}
.leaguecomponent{
  font-size: 20px;
  font-family: Arial, Helvetica, sans-serif;
  color: #88f29b;
}
.leaderboardDisplay{
  background-color: white;
}
</style>