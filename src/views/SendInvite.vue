<template>
    <div class= "sendInvite">
        <br>
        <send-invite/>
    </div>
</template>

<script>

import SendInvite from '@/components/SendInvite.vue'

export default {
    components:
    {
        SendInvite
    }
}
</script>
<style>
.sendInvite{
    display: flex;
    justify-content: center;
  font-family: 'Copperplate';
  color: #2d487a;
  font-size: 30px; 
  height: 100%; 
  background-color: whitesmoke;

}
</style>