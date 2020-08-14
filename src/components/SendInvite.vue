<template>
    <div class = "form">
        <form>
<br>
<label for="Send To">Send To:</label><br>
  <input type="text"  v-model="email.toEmail"/><br><br>
<label>Subject:</label>
<input type="text" v-model="email.subject"/><br><br>
<label>Body:</label>
<input type="text" v-model="email.body"/><br><br>
    <button class="btn btn-submit" v-on:click="sendInvite" >Submit</button>
        </form><br>
    </div>
</template>

<script>
import authService from '@/services/AuthService.js';

export default {

  data(){
      return{
          email :{
          toEmail: '',
          subject: '',
          body: '',
          }
      }
  },

    methods: {
      sendInvite() {
      authService.sendEmail(this.email).then(response=>{
             alert(response.status + "Your email has been sent successfully!")
            }
         ).catch(error => {alert("Error")})
      }
    }
}

</script>
<style scoped>
.form{
    display: flex;
    justify-content: center;
  font-family: 'Copperplate';
  color: #2d487a;
  font-size: 30px; 
  height: 100%; 
  background-color: whitesmoke;

}
</style>
