<template>
    <div class="CONTACT-Content">
        <div class="phone">
            <h2 style="color: white;">Phone</h2>
            <p>(04) 1234 5678</p>
        </div>

        <br>

        <ul></ul>

        <br>

        <div class="location">
            <h2 style="color: white;">Location</h2>
            <p>221 Burwood Hwy, Burwood VIC 3125</p>
        </div>

        <br>

        <ul></ul>

        <br>

        <div class="time">
            <h2 style="color: white;">Openning Hours</h2>
            <div class="week">
                <h4 style="color: white;">Monday - Friday</h4>
                <p>9:00am - 5:30pm</p>
            </div>
            <div class="week">
                <h4 style="color: white;">Saturday</h4>
                <p>10:30am - 3:00pm</p>
            </div>
            <div class="week">
                <h4 style="color: white;">Sunday</h4>
                <p>Closed</p>
            </div>
        </div>

    </div>
</template>


<style>
.CONTACT-Content {
    margin: 0 auto;
    max-width: 800px;
    display: flex;
    justify-content: space-between;
    gap: 5px;

    background-color: rgba(49, 44, 44, 0.311);
    padding: 40px;
}

.week {
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    gap: 20px;
    

}

ul {
    text-align: center;
    padding: 0; /* Remove default padding */
    margin: 0; /* Remove default margin */
    border-left: 1px solid rgb(101, 228, 185); /* Add a left border for the vertical line */
    padding-left: 10px;
}


</style>