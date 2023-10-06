<template>

<br><br>

<video width="100%" controls>
    <source src="video/Bugatti.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

    <br><br>

    <div class="about-content">
        <img id="about-image" src="/image/a.jpeg" alt="About">
        <div class="about-text">

            <br>

            <h2 style="color: rgb(101, 228, 185);">Prestige experience and vehicle specialist</h2>
            
            <br>

            <p>Prestige Lane is a luxury vehicle delearship specialised in selling a wide range of Exotic cars. Located in the heart of Melbourne, we are commited to providing quality service to all of our customers. It also offers a diverse scope of purchasing and leasing options to meet everyone's needs. With our finance options, every one of our customrers can buy the vehicle of their dreams.</p>
            <p>Ready to set up a test drive? Stop by Prestige Lane and get behind the driver’s seat today.</p>
        
            <br>

            <!-- <RouterLink to="/shop">
                <button>Find the right vehicle</button>
            </RouterLink>     -->

            <br>

        </div>

    </div>

    <br>

</template>

<style>
.about-text {
    padding: 20px; /* Adds padding to create space around the content */
    text-align: center; /* Centers the text horizontally */
    color: rgb(255, 255, 255);
    max-width: 400px;
    margin: 0 auto;

}

.about-content {
    display: flex; /* Use flexbox for layout */
    max-width: 1000px; /* Limits the width of the content container */
    margin: 0 auto; /* Centers the content horizontally */
    text-align: center;

    /* background-color: rgb(29, 30, 31); */
    padding: 20px;

}

#about-image {
    max-width: 40%; /* Ensure the image doesn't exceed the width of its container */
    max-height: 40%; /* Ensure the image doesn't exceed the height of its container */
    width: auto; /* Allow the image to scale proportionally */
    height: auto; /* Allow the image to scale proportionally */

    margin: 0 auto;
}
</style>