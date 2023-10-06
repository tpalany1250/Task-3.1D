<template>

    <br>

    <div class="logo-header">
        <h1 style="margin-left: -120px;">Popular Makes</h1>
    </div>

    <br>

    <div class="logos">

        <article class="badge">
           
            <img src="/image/rolls-royce.png"
            width="70%">

        </article>

        <article class="badge">
          
            <img src="/image/bentley.png"
            width="80%">

        </article>

        <article class="badge">
           
            <img src="/image/lotus.png"
            width="70%">

        </article>

        <article class="badge">
           
            <img src="/image/maybach.png"
            width="110%">


        </article>

        <article class="badge">
          
            <img src="/image/koenigsegg.png"
            width="65%">

        </article>

        <article class="badge">
           
            <img src="/image/mercedes.png"
            width="95%">

        </article>

        <article class="badge">
            
            <img src="/image/maserati.png"
            width="80%">

        </article>

        <article class="badge">
          
            <img src="/image/mclaren.png"
            width="110%">

        </article>

        <article class="badge">

            <img src="/image/bugatti.png"
            width="80%">

        </article>

        <article class="badge">
         
            <img src="/image/aston-martin.png"
            width="90%">

        </article>

        <article class="badge">

            <img src="/image/porsche.png"
            width="100%">

        </article>

        <article class="badge">
           
            <img src="/image/lamborghini.png"
            width="110%">

        </article>

        <article class="badge">
        
            <img src="/image/ferrari.png"
            width="95%">

        </article>

        <article class="badge">
          
            <img src="/image/bmw.png"
            width="60%">

        </article>

        <article class="badge">
         
            <img src="/image/jaguar.png"
            width="85%">

        </article>

        <article class="badge">
        
            <img src="/image/audi.png"
            width="80%">

        </article>

    </div>

    <br>

    <p style="text-align: center;"><div v-html="Instruction"></div>
 </p>



</template>


<script>
export default {
  data() {
    return {
      Instruction: '<span style="color: white; font-weight: bold;">Look through our featured products to experience our luxury</span>',
    }
  }

}
</script>


<style>
.logo-header {
    color: white;
}

@media (min-width: 768px) {
    .logo-header {
        margin-left: 200px;
    }
}

.logos {
    display: flex;
    margin: 10px;
    padding: 10px;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
}

.badge {
    border: 2px solid #2e2a2a;
    border-radius: 10px;
    margin: 10px;
    padding: 10px;
    width: 140px;
    height: 115px;
    text-align: center;
    background-color: rgb(255, 255, 255);

    display: flex; /* Use flexbox for centering */
    flex-direction: column; /* Stack image and text vertically */
    justify-content: center; /* Center items vertically */
    align-items: center; /* Center items horizontally */
}
</style>