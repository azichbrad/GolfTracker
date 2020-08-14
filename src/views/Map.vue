<template>
    <div>
        <div style="display: flex; align-items: center; justify-content: space-evenly">
<p>
     
    </p>
         </div>
        <GmapMap
            :center="myCoordinates"
            :zoom="7"
            style="width:640px; height:360px; margin: 32px auto;"
            ref="mapRef"
        ></GmapMap>
    </div>
</template>

<script>
export default {
    data(){
        return{
            map: null,
            myCoordinates:{
                lat: 0,
                lng: 0
            }
        }
    },
    created(){
        this.$getLocation({})
            .then(coordinates => {
                this.myCoordinates = coordinates;
            })
            .catch(error=> alert(error));
    },
    mounted(){
            this.$refs.mapRef.$mapPromise.then(map => this.map = map);
    },
    computed: {
          mapCoordinates() {
              if(!this.map) {
                  return{
                    lat: 0,
                    lng: 0
                  };
              }
              return{
                  lat: this.map.getCenter().lat().toFixed(3),
                  lng: this.map.getCenter().lng().toFixed(3)
              }
          }
    }
}
</script>