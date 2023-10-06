<template>
    
    <div class="logo-header">
        <h1 style="margin-left: -120px;">Featured</h1>
    </div>

    <br>

    <div class="catalog">

        <article class="product" v-for="(product, productIndex) in displayedProducts" :key="productIndex">
            <div class="image-container">
        
                <div class="arrow left-arrow" @click="changeImage(productIndex, 'prev')">←</div>
                <img :src="product.images[product.currentImageIndex]" :alt="product.name" />
                <div class="arrow right-arrow" @click="changeImage(productIndex, 'next')">→</div>
            </div>

            <div class="product-text">
                <p>${{ product.price }}</p>
                <h3>{{ product.name }}</h3>
              
            </div>
        </article>
    </div>

    <!-- Pagination buttons -->
    <div class="pagination">
      <button @click="previousPage" :disabled="currentPage === 0">Previous</button>
      <button @click="nextPage" :disabled="currentPage === totalPages - 1">Next</button>
    </div>
</template>


<script>
export default {
  data() {
    return {
      products: [
        {
          name: '2023 Maserati MC20 Auto MY22',
          location: 'Product description here...',
          price: '505,000',
          images: [
            '/image/P1/1.1.jpeg',
            '/image/P1/1.2.jpeg',
            '/image/P1/1.3.jpeg',
            '/image/P1/1.4.jpeg',
            '/image/P1/1.5.jpeg',
            '/image/P1/1.6.jpeg',
            '/image/P1/1.7.jpeg',
            '/image/P1/1.8.jpeg',
            ],
            currentImageIndex: 0,
        },
        // Add more product data as needed
        {
          name: '1992 Ferrari 512tr Manual',
          location: 'Product description here...',
          price: '309,900',
          images: [
            '/image/P5/5.1.jpeg',
            '/image/P5/5.2.jpeg',
            '/image/P5/5.3.jpeg',
            '/image/P5/5.4.jpeg',
            '/image/P5/5.5.jpeg',
            '/image/P5/5.6.jpeg',
            ],
            currentImageIndex: 0, // Track current image index for this product
        },
        {
          name: '2012 Aston Martin DB9 Auto MY12',
          location: 'Product description here...',
          price: '144,950',
          images: [
            '/image/P3/3.1.jpeg',
            '/image/P3/3.2.jpeg',
            '/image/P3/3.3.jpeg',
            '/image/P3/3.4.jpeg',
            '/image/P3/3.5.jpeg',
            '/image/P3/3.6.jpeg',
            ],
          currentImageIndex: 0,
        },
        {
          name: '1993 Jaguar XJ220 Manual',
          location: 'Product description here...',
          price: '1,050,000',
          images: [
            '/image/P4/4.1.jpeg',
            '/image/P4/4.2.jpeg',
            '/image/P4/4.3.jpeg',
            '/image/P4/4.4.jpeg',
            '/image/P4/4.5.jpeg',
            '/image/P4/4.6.jpeg',
            ],
          currentImageIndex: 0,
        },
        {
          name: '2014 Rolls-Royce Wraith Auto',
          location: 'Product description here...',
          price: '399,990',
          images: [
          '/image/P2/2.1.jpeg',
            '/image/P2/2.2.jpeg',
            '/image/P2/2.3.jpeg',
            '/image/P2/2.4.jpeg',
            '/image/P2/2.5.jpeg',
            '/image/P2/2.6.jpeg',
            '/image/P2/2.7.jpeg',
            ],
            currentImageIndex: 0, // Track current image index for this product
        },
        {
          name: '1926 Bentley 3 Litre Manual',
          location: 'Product description here...',
          price: '898,900',
          images: [
            '/image/P4/4.1.jpeg',
            '/image/P4/4.2.jpeg',
            '/image/P4/4.3.jpeg',
            '/image/P4/4.4.jpeg',
            '/image/P4/4.5.jpeg',
            '/image/P4/4.6.jpeg',
            ],
          currentImageIndex: 0,
        },
        {
          name: '2018 Mercedes-Benz S-Class Maybach S650 Auto',
          location: 'Product description here...',
          price: '499,990',
          images: [
          '/image/P2/2.1.jpeg',
            '/image/P2/2.2.jpeg',
            '/image/P2/2.3.jpeg',
            '/image/P2/2.4.jpeg',
            '/image/P2/2.5.jpeg',
            '/image/P2/2.6.jpeg',
            '/image/P2/2.7.jpeg',
            ],
            currentImageIndex: 0, // Track current image index for this product
        },
        {
          name: '2022 McLaren 765LT Auto MY22',
          location: 'Product description here...',
          price: '959,000',
          images: [
            '/image/P3/3.1.jpeg',
            '/image/P3/3.2.jpeg',
            '/image/P3/3.3.jpeg',
            '/image/P3/3.4.jpeg',
            '/image/P3/3.5.jpeg',
            '/image/P3/3.6.jpeg',
            ],
          currentImageIndex: 0,
        },
        {
          name: '1972 BMW 3.0 CSL E9 Manual',
          location: 'Product description here...',
          price: '495,000',
          images: [
            '/image/P4/4.1.jpeg',
            '/image/P4/4.2.jpeg',
            '/image/P4/4.3.jpeg',
            '/image/P4/4.4.jpeg',
            '/image/P4/4.5.jpeg',
            '/image/P4/4.6.jpeg',
            ],
          currentImageIndex: 0,
        },
        {
          name: '1993 Porsche 911 Turbo 964 Manual',
          location: 'Product description here...',
          price: '399,990',
          images: [
          '/image/P2/2.1.jpeg',
            '/image/P2/2.2.jpeg',
            '/image/P2/2.3.jpeg',
            '/image/P2/2.4.jpeg',
            '/image/P2/2.5.jpeg',
            '/image/P2/2.6.jpeg',
            '/image/P2/2.7.jpeg',
            ],
            currentImageIndex: 0, // Track current image index for this product
        },
        {
          name: '1993 Jaguar XJ220 Manual',
          location: 'Product description here...',
          price: '1050000',
          images: [
            '/image/P4/4.1.jpeg',
            '/image/P4/4.2.jpeg',
            '/image/P4/4.3.jpeg',
            '/image/P4/4.4.jpeg',
            '/image/P4/4.5.jpeg',
            '/image/P4/4.6.jpeg',
            ],
          currentImageIndex: 0,
        },
        {
          name: '1993 Jaguar XJ220 Manual',
          location: 'Product description here...',
          price: '1050000',
          images: [
            '/image/P4/4.1.jpeg',
            '/image/P4/4.2.jpeg',
            '/image/P4/4.3.jpeg',
            '/image/P4/4.4.jpeg',
            '/image/P4/4.5.jpeg',
            '/image/P4/4.6.jpeg',
            ],
          currentImageIndex: 0,
        },
      ],
      currentPage: 0, // Current page index
      itemsPerPage: 6, // Number of items per page
    };
  },
  computed: {
    totalPages() {
      return Math.ceil(this.products.length / this.itemsPerPage);
    },
    displayedProducts() {
      const start = this.currentPage * this.itemsPerPage;
      const end = start + this.itemsPerPage;
      return this.products.slice(start, end);
    },
  },
  methods: {
    changeImage(productIndex, direction) {
      const product = this.displayedProducts[productIndex];
      if (direction === 'prev') {
        product.currentImageIndex =
          (product.currentImageIndex - 1 + product.images.length) % product.images.length;
      } else if (direction === 'next') {
        product.currentImageIndex = (product.currentImageIndex + 1) % product.images.length;
      }
    },
    previousPage() {
      if (this.currentPage > 0) {
        this.currentPage--;
      }
    },
    nextPage() {
      if (this.currentPage < this.totalPages - 1) {
        this.currentPage++;
      }
    },
  },
};
</script>


<style>

.catalog {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.product {
    border: 1px solid #827d7d;
    margin: 10px;
    /* padding: 10px; */
    flex: calc(33.33% - 20px); /* 33.33% width for each product with 20px margin in between */
    height: 350px;
    /* text-align: center; */
    overflow: hidden;
    display: flex;
    flex-direction: column;
    position: relative;
}

.product img {
  max-width: 100%; /* Limit image width to 100% of the container */
  max-height: 100%; /* Limit image height to 100% of the container */
  /* transition: transform 0.3s ease; */
}

.image-container {
  flex: 1;
  display: flex;
  flex-direction: column;
  text-align: center; /* Center the image horizontally within the container */
}

.arrow {
  position: absolute;
  top: 50%;
  font-size: 24px;
  cursor: pointer;
  color: rgba(0, 0, 0, 0.5); /* Set arrow color */
  transition: color 0.3s; /* Add transition effect for arrow color change */
}

.left-arrow {
  left: 10px; /* Adjust the position of the left arrow */
}

.right-arrow {
  right: 10px; /* Adjust the position of the right arrow */
}

.arrow:hover {
  color: rgb(101, 228, 185); /* Change to your desired hover color */
}


.product-text {
    /* position: absolute;
    bottom: 0; /* Align the text to the bottom 
    left: 0; /* Align the text to the left 
    right: 0; Align the text to the right */
    background-color: rgb(255, 255, 255);
    color: rgb(46, 43, 43); /* Set text color */
    padding: 10px; /* Adjust padding as needed */
}

/* Media query for responsiveness */
@media (max-width: 768px) {
  .catalog {
    flex-direction: column;
  }

  .product {
    width: 100%; /* Full width for each product on smaller screens */
  }
}

/* Add styles for pagination buttons */
.pagination {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}

.pagination button {
  background-color: rgb(101, 228, 185);
  color: #fff;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  margin: 0 10px;
}

.pagination button:disabled {
  background-color: #ccc;
  cursor: not-allowed;
}

</style>