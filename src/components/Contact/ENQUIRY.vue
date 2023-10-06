<template>
  <div class="container">

  <div class="enquiry">
    <p>Enter your name: </p>
    <input type="text" v-model="formData.name" />

      <br><br>

    <p>Enter your email: </p>
    <input type="text" v-model="formData.email" />
  
    <br><br>

    <p>Enter your phone number: </p>
    <input type="text" v-model.number="numericValue" />
    
    <br><br>

    <p>What would you like to enquire about:</p>
    <div class="enquiry-form">

        <input type="radio" id="E" value="Financing" v-model="checkedNames" />
        <label for="E">Financing</label>

        <br>

        <input type="radio" id="G" value="Our Vehicles" v-model="checkedNames" />
        <label for="G">Our Vehicles</label>

        <br>

        <input type="radio" id="M" value="Our Collectibles" v-model="checkedNames" />
        <label for="M">Our Collectibles</label>

        <br>

        <input type="radio" id="Pass" value="Other" v-model="checkedNames" />
        <label for="Pass">Other</label>

    </div>

    <br>

    <p>Additional Details</p>
    <textarea v-model.lazy="formData.comment"></textarea>

    <br><br>
  
    <!-- Button to confirm the comment -->
    <button @click="confirmComment">Confirm</button>

  </div>

  <div class="output">
    <p>Name: {{ formData.name }}</p>

    <p>Email: {{ formData.email }}</p>

    <p>Phone number: {{ numericValue }}</p>

    <p>Enquiry: {{ checkedNames }}</p>

    <p>Additional Details: {{ confirmedComment }}</p>

    <input type="submit" value="Submit" style="width: 80px;">

  </div>


  <br><br>

</div>
  
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: "",
        email: "",
        message: "",
        comment: "", // Add a comment field to formData
      },
      numericValue: 0,
      checkedNames: [],
      confirmedComment: "",
    };
  },
  methods: {
    submitForm() {
      // Handle form submission here
      console.log("Form submitted:", this.formData);
      // Sends the data to the server or perform any other actions
    },
    confirmComment() {
      // Handle comment confirmation here
      this.confirmedComment = this.formData.comment;
    },
  },
};
</script>

<style>
.container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start; /* Adjust alignment as needed */
}

.enquiry {
  flex: 1; /* This makes the "enquiry" div expand to fill available space */
  padding: 20px; /* Add padding to separate the sections */
}

.output {
  flex: 1; /* This makes the "output" div expand to fill available space */
  padding: 20px; /* Add padding to separate the sections */
}


form {
    margin: 0 auto;
    max-width: 800px;
    color: white;
}

input {
    padding: 10px;
}

.enquiry p {
  color: white;
  line-height: 3.5;
}

.enquiry-form {
  line-height: 2;
}

.output p {
  color: white;
  line-height: 3;
}


</style>