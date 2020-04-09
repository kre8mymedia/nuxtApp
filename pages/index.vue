<template>
 <div class="px-0 container-fluid">
    <Navbar></Navbar>
    <div class="container pt-5 text-center">
      <h1>Welcome to Thesis</h1>
      <small><i>An Adaptive Technologies Company</i></small>
      <p>Welcome to my sample NuxtJS App<br>with Bootstrap CDN</p>
      <img class="mt-5" height="300px" src="https://siasky.net/vAEumK81Jb3xnTLv8HuyJMf3i0sjNof_1x5sdh0WjOnOJw" alt="Adaptive Tech Logo">
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar';

export default {
  components: {
    'Navbar': Navbar
  }
}
</script>

<style>
  html {
    height: 100%;
  }
  a {
    color: white !important;
  }
  body {
    color: white;
    background: linear-gradient(#201866, #000000);
  }
</style>
