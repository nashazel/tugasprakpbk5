<template>
  <div>
    <Navbar />
    <div class="container mt-4">
      <Carousel />
      <div class="card-container mt-4">
        <Card 
          v-for="product in products" 
          :key="product.id" 
          :title="product.name" 
          :description="product.description" 
          :url="product.url" 
        />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Ibanez GSA60', 
          description: 'Musical Instrument of your dreams.', 
          url: 'https://cdn1.productnation.co/optimized/1024w/stg/sites/5/5d4d032387117.webp' 
        },
        { 
          id: 2, 
          name: 'Yamaha Pacifica', 
          description: 'Musical Instrument of your dreams.', 
          url: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjOqTVbIljTFuIMCQQJFjPa7vKqYIx5RqC06-XEYntbcQfhgpmppdzmnOPusCC9GF9b9TAZ8aExmeyt9oqzoiNQrsAWWi4O8tW7KGphJQhxWynoa33c9lTiDDU0vgWhqR8IfPrfmVeedcWw/s1600/F143F40893964D5EBBBA50E73698533C_12073.jpg' 
        },
        { 
          id: 3, 
          name: 'Epiphone Les Paul',
          description: 'Musical Instrument of your dreams.', 
          url: 'https://www.stars-music.com/medias/epiphone/les-paul-standard-ch-ebony-hd-53970.webp' 
        },
        { 
          id: 4, 
          name: 'Rockwell SCG-01', 
          description: 'Musical Instrument of your dreams.', 
          url: 'https://cdn1.productnation.co/stg/sites/5/61f0b9358ae80.jpeg' 
        },
        { 
          id: 5, 
          name: 'Schecter Omen Extreme-6', 
          description: 'Musical Instrument of your dreams.', 
          url: 'https://schecter-shop.ru/wa-data/public/shop/products/98/09/998/images/2660/2660.970.jpg' 
        },
        { 
          id: 6, 
          name: 'Squier Affinity Stratocaster', 
          description: 'DMusical Instrument of your dreams.', 
          url: 'https://mg.co.id/wp-content/uploads/2023/06/Squier-FSR-Affinity-Series-Stratocaster-QMT-Electric-Guitar-Laurel-FB-Sapphire-Blue-Transparent.jpg' 
        }
      ]
    };
  }
};
</script>

<style>
body {
  background-color: rgb(239, 234, 234);
}

.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 16px; /* Optional: Adjust the space between cards */
}

.card {
  flex-basis: calc(33.33% - 16px); /* Atur lebar kartu dengan ketiga bagian dari wadah dikurangi jarak antar kartu */
}
</style>
