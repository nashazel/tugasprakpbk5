<template>
  <div class="carousel">
    <div v-for="(image, index) in images" :key="index" class="carousel-item">
      <img :src="image.url" :alt="image.alt" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  data() {
    return {
      images: [
        { url: 'https://www.bajaao.com/cdn/shop/files/esp-electric-guitars-esp-ltd-gl-200k-george-lynch-kamakaze-1-electric-guitar-15659486147_500x.jpg?v=1687997562', alt: 'Joyride Sneakers' },
        { url: 'https://theguitarworld.com/cdn/shop/products/syn-custom-s-sgb-w-pickup-1743-neck-joint-high8_2000x.jpg?v=1579589904', alt: 'Image 2' },
        { url: 'https://m.media-amazon.com/images/I/614aE0tg4fL.jpg', alt: 'Image 3' }
      ]
    }
  }
}
</script>

<style>
.carousel {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  padding: 10px ; /* Padding atas dan bawah */
  margin-bottom: 20px; /* Jarak bawah */
}

.carousel-item {
  scroll-snap-align: start;
  flex: none;
  width: 100%; /* Lebar item carousel */
  margin-right: 10px; /* Jarak antar item */
  border-radius: 8px; /* Sudut bulat */
  overflow: hidden; /* Mengatasi overflow */
}

.carousel-item img {
  width: 100%; /* Lebar gambar */
  max-height: 500px; /* Tinggi maksimum gambar */
  object-fit: cover; /* Memastikan gambar mengisi seluruh area */
  border-radius: 8px; /* Memberikan sudut bulat pada gambar */
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); /* Efek bayangan untuk tampilan yang lebih menarik */
  transition: transform 0.3s ease; /* Efek transisi saat gambar dihover */
}

.carousel-item:hover img {
  transform: scale(1.05); /* Memperbesar gambar saat dihover */
}

@media (max-width: 768px) {
  .carousel-item {
    width: 90%; /* Lebar item carousel untuk tampilan mobile */
  }
}
</style>
