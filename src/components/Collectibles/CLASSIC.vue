<template>

    <div class="classic-content">
        <div class="collectibles-container">
            <img id="classic-image" src="/image/CLASSIC.jpg" alt="classic" style="width: 100%;">
        </div>
        <div class="text-container">
            <br>
            <h1>Classic Cars</h1>
            <p>This is a samle text</p>

            <br>

            <p>The Classic Sports Cars have a sleek and stylish look that is sure to stop everyone in the streets. One of the best vehicles on the market in terms of maintaining value, our Classic Sports Cars are safe, reliable, and a great choice for everyone. This vehicles is calling your name, are you ready to answer? Come test drive it today.</p>
        </div>
    </div>

</template>


<style>
.classic-content {
    margin: 0 auto;
    max-width: 1200px;
    color: white;
    display: flex;
}

.collectibles-container {
    flex: 1; /* Take up 50% of the container width */
    padding: 10px; /* Optional: Add padding for spacing */
    max-width: 600px;
}

.text-container {
    flex: 1; /*Take up 50% of the container width */
    padding: 30px; /* Optional: Add padding for spacing */
    max-width: 600px;

    text-align: center;
}

</style>