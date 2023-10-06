<template>

    <div class="collectibles-background">

        <img style="height: 100px;">

        <br>

        <div class="collectibles-content">

        <!-- <div class="image-container"> -->
            <img id="collectibles-image" src="/public/image/c1.webp" alt="Collectibles">
        <!-- </div> -->
        
            <div class="collectibles-text">

                <br><br>

                <h1 style="font-size: 60px; line-height:0%;">Collectibles</h1>
                <!-- <p>If you like what you see on</p> -->
                <br><br><br><br><br><br><br><br>
                
                <RouterLink to="/collectibles">
                    <button>Learn more</button>
                </RouterLink>
            </div>
        </div>

        <br><br>

    </div>

</template>


<style>
.collectibles-background {
    background-image: url('/image/b.jpg');
    background-size: cover; /* Cover the entire container */
    background-position: top left; /* Align the background image to the top left corner */
    background-repeat: no-repeat;

    margin-left: -40px;
    margin-right: -32px;
}

.collectibles-content {
    /* display: flex; Use flexbox for layout */
    max-width: 1100px; /* Limits the width of the content container */
    margin: 0 auto; /* Centers the content horizontally */
    text-align: center;

    /* justify-content: center; */

    background-color: #1c1c1c;
    padding: 20px;
    /* position: relative; */
}

#collectibles-image {
    max-width: 100%; /* Ensure the image doesn't exceed the width of its container */
    /* max-height: 80%; Ensure the image doesn't exceed the height of its container */
    width: auto; /* Allow the image to scale proportionally */
    height: auto; /* Allow the image to scale proportionally */

    margin: 0 auto;
}

.collectibles-text {
    /* position: relative; Position the text absolutely within the .collectibles-content */
    /* top: 0;
    left: 0; */
    /* right: 260px; Make the text span the entire width of .collectibles-content */
    /* bottom: 80px; Make the text span the entire height of .collectibles-content */
    /* background-color: rgba(255, 255, 255, 0.8); Optional: Add a background color with some opacity for readability */
    padding: 40px; /* Optional: Add padding to the text for better spacing */
    /* display: flex; */
    /* flex-direction: column; */
    /* justify-content: center;
    align-items: center; */


    background-color: rgb(18, 19, 19);


    line-height: 0.5;
    color: rgb(101, 228, 185);

    max-width: 100%;
    text-align: center;
    margin: 0 auto;



    /* background-color: #262424; */

}
</style>