<script setup>
import HEADERCOLLECTIBLES from '../components/Collectibles/HEADERCOLLECTIBLES.vue';
import CLASSIC from '../components/Collectibles/CLASSIC.vue';
import COLLECTOR from '../components/Collectibles/COLLECTOR.vue';
import VINTAGE from '../components/Collectibles/VINTAGE.vue';
</script>

<template>

    <HEADERCOLLECTIBLES />

    <br><br><br><br>

    <CLASSIC />

    <br><br><br>

    <COLLECTOR />

    <br><br><br>

    <VINTAGE />

    <br><br><br>
    
    <div class="border">
        <div class="collectibles-next">

            <p> Don't miss out on your chance to own your very first collectible, {{ num1 }} out of {{ num2 }} people miss this opportunity. Be part of that {{ num2 - num1}}% club</p>

            <br>
            
            <RouterLink to="/contact">
                <button>Contact Us</button>
            </RouterLink>
        </div>
    </div>
    
    <br><br><br>

</template>


<script>
export default {
  data() {
    return {
      num1: 9,
      num2: 10,
    }
  }

}
</script>

<style>

.collectibles-next {
    margin: 0 auto;
    max-width: 800px;
    color: #ffffff;
    padding: 20px;
    text-align: center;
    border: 4px solid #ffffff;
    border-radius: 10px;
}

/* .border {
    margin: 0 auto;
    max-width: 800px;
    border: 2px solid #ffffff;
    border-radius: 10px;
} */
</style>