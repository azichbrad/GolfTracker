<template>
    <div class= "leagues">
        <league/>
        <Leagues/>

    </div>
</template>

<script>
import League from "@/components/League.vue";
import Leagues from "@/components/Leagues.vue";

export default {
    name: 'leagues',
    components:
    {
        Leagues,
        League
    }
}
</script>