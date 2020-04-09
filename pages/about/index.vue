<template>
  <div class="px-0 container-fluid">
    <Navbar></Navbar>
    <div class="pt-5 text-center container">
      <h1>About Page</h1>
      <p>This is the about page, this app is a sample app that has been preconfigured with Bootstrap CDN!</p>
      <img class="mt-5" height="300px" src="https://siasky.net/PADdiPhorWOZaLkVmbIsjF0lW1DRR7fueYEJBqMiK-woUA" alt="Adaptive Tech Logo">
    </div>
  </div>
</template>

<script>
import Navbar from '../../components/Navbar';

export default {
  components: {
    'Navbar': Navbar
  }
}
</script>