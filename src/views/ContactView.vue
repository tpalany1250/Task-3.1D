<script setup>
import CONTACT from '../components/Contact/CONTACT.vue';
import ENQUIRY from '../components/Contact/ENQUIRY.vue';
import MAP from '../components/Contact/MAP.vue';
</script>

<template>

    <br><br><br><br>

    <div class="contact-header">
        <h1>Contact Us</h1>
    </div>


    <br>
    
    
    <CONTACT />
    
    
    <br><br>


    <div class="map-header">
        GOOGLE MAP
    </div>

    <br>

    <MAP/>
    
    <br><br>

    <div class="contact-header">
        <h1>Enquiry Form</h1>
    </div>

    <br>

    <ENQUIRY />

    <br><br><br><br>

</template>



<style>
.contact-header {
    margin: 0 auto;
    max-width: 800px;
    color: white;
}

.map-header {
    margin: 0 auto;
    max-width: 1100px;
}

</style>