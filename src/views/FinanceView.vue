<script setup>
import HEADERFINANCE from '../components/Finance/HEADERFINANCE.vue';
import FINANCING from '../components/Finance/FINANCING.vue';
import LEASING from '../components/Finance/LEASING.vue';
import TRADE from '../components/Finance/TRADE-IN.vue';
</script>


<template>

    <HEADERFINANCE />

    <br><br><br>

    <div class="f-text">
        <h1>Benefits & Services</h1>
    </div>
    
    <br>

    <FINANCING />

    <br><br>

    <LEASING />

    <br><br>

    <TRADE />

    <!-- <br><br> -->

    <!-- <div class="finance-next">
        <button>Contact Us</button>
    </div> -->

    <br><br><br>

    <p style="text-align: center; color: rgb(255, 255, 255);">Watch the video to understand how you could finance your next dream car</p>

    <br>

    <div class="finance-video">
        <iframe width="60%" height="450px" src="https://www.youtube.com/embed/_FLbikg8uj8" frameborder="0" allowfullscreen></iframe>
    </div>

    <br><br><br>

</template>

<style>

.finance-header {
    padding: 40px;
    text-align: center;
    color: rgb(101, 228, 185);
    background-color: rgb(20, 18, 18);
}

.finance-video {
    display: flex;
    justify-content: center;
}

.finance-next {
    text-align: center;
}

.f-text {
    color: #ffffff;
    text-align: center;
}

</style>