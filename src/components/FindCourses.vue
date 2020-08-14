<template>
    <div class="all">
        <div>
        <Map/><br>
        </div>
    <form class = "radius">
  <label for="radius">Choose a Radius:</label>
  <select name="Radius" id="radius">
    <option value="5">5 miles</option>
    <option value="10">10 miles</option>
    <option value="20">20 miles</option>
    <option value="50">50 miles</option>
  </select>
  </form>
    </div>
</template>


<script>

import Map from '@/views/Map';
export default {
  name: 'Home',
  components:{
    Map
  }
  

}
  



</script>
<style scoped>
 .radius{
    display: flex;
    justify-content: center;
} 
.all{

    display: flex;
    justify-content: center;
  font-family: 'Copperplate';
  color: #2d487a;
  font-size: 30px; 
  height: 100%; 
  background-color: whitesmoke;

}

</style>