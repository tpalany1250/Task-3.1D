<template>

    <div class="collectibles-banner">
        <img style="height: 100px;">
        <h1>Collectibles</h1>
    </div>

</template>

<style>
/* .shop-banner {
    background-color: aquamarine;
    color: white;
    padding: 150px;
    margin-left: -40px;
    margin-right: -32px;
    font-size: larger;
    } */


.collectibles-banner {
    /* position: relative; Set the container to relative positioning */
    /* background-color: aquamarine; */
    background-image: url('/image/m.jpg');
    background-size: cover; /* Cover the entire container */
    background-position: top left; /* Align the background image to the top left corner */
    background-repeat: no-repeat;
    
    color: white;
    padding: 150px;
    margin-left: -40px;
    margin-right: -32px;
    font-size: larger;
}

.collectibles-banner h1 {
    /* position: relative; Set the text to absolute positioning */
    /* top: 50%; Position it in the middle vertically */
    /* left: 50%; Position it in the middle horizontally */
    /* transform: translate(-50%, -50%); Center it precisely */
    z-index: 1; /* Ensure the text is above the image */
}
</style>