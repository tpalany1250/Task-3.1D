<template>

    <br><br>

    <div class="finance-content">

        <div class="finance-text">
            <h2 style="color: rgb(101, 228, 185);">Want to finance your prestige vehicle?</h2>
            
            <br>
            
            <p>Finance teams are available at Prestige Lane to best support customers with the vehicle of their dreams. Whether new or pre-owned, we’re sure to have something in stock to meet everyone’s needs.</p>
        
            <br>
        
            <RouterLink to="/finance">
                <button>See Options</button>
            </RouterLink>

        </div>
    </div>

    <br><br><br>

</template>


<style>

.finance-content {
    display: flex; /* Use flexbox for layout */
    max-width: 1000px; /* Limits the width of the content container */
    margin: 0 auto; /* Centers the content horizontally */
    text-align: center;

    /* background-color: rgb(29, 30, 31); */
    padding: 20px;
    color: white;
}

</style>