<template>
  <nav class="navbar">
    <div class="logo">Nasha's Music</div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#products">Products</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style>

.navbar {
  display: flex;
  font-family: 'Poppins';
  justify-content: space-between;
  align-items: center; /* Rata tengah secara vertikal */
  background-color: #262c2d;
  padding: 10px;
}

.logo {
  color: #ffffff;
  font-size: 24px;
  font-family: 'Poppins'
  
}
.nav-links {
  list-style: none;
  display: flex;
}
.nav-links li {
  margin: 0 10px;
}
.nav-links a {
  color: #fff;
  text-decoration: none;
}


</style>
