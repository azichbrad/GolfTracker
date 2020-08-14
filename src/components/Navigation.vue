<template>
  <div v-if="$store.state.token != ''">
    <nav class="nav">
      <router-link v-bind:to="{ name: 'home' }">Home</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'send' }">Send Invite</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'join' }">Join League</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'addcourse' }">Register Course</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'locate' }">Find Courses</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'leaderboard' }">Leader Board</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'post' }">Post Scores</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'create' }">Create League</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'logout' }">Logout</router-link>
    </nav>
  </div>
</template>

<style> 
  .spacing { 
    margin: 10px;
  } 

  a:link{
    text-decoration: none;
    color: #1b3869;
  }

  a:visited{
    color: #1b3869;
  }
  
</style>

// #88f29b