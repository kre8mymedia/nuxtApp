<template>
  <div class="px-0 container-fluid">
    <!-- Navbar -->
    <Navbar :isLoggedin="isLoggedin"></Navbar>
    <!-- END Navbar -->

    <!-- MAIN CONTENT -->
    <div class="row justify-content-center">
      <div class="col-sm-4">

        <!-- Header Stuff -->
        <div class="text-center">
          <img height="300px" src="~/assets/black-logo.png" alt="Adaptive Tech Logo">
          <h2>Retrieve Password</h2>
          <p>Please enter an email address<br>to send new password</p>
        </div>
        <!-- END Header Stuff -->

        <!-- Retreival Email -->
        <div v-if="isLoggedin == false" class="pt-1 pb-1 container">
            <div class="form-group">
              <label for="exampleInputEmail1">Email address</label>
              <input v-model="email" type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
              <small class="form-text text-muted"><font id="emailHelp" color="red"></font></small>
            </div>
            <button v-on:click="login()" type="button" class="btn btn-primary">Submit</button>
        </div>
        <!-- END Retreival Email -->

      </div>
    </div>
    <!--END MAIN CONTENT -->

  </div>
</template>

<script>
import Navbar from '../../components/Navbar';

export default {
  components: {
    Navbar
  },
  data() {
    return{
      email: "",
      password: "",
      isLoggedin: false,
    }
  },
  methods: {
    login() {
      if (this.email != "" && this.password != "") {
        if (this.email == 'test@test.com' && this.password == 'test1234') {
          this.isLoggedin = true
          console.log(this.email, this.password)
        } else {
          document.getElementById('emailHelp').innerHTML = "You have entered an invalid login!";
        }
      } else {
        console.log("please enter email and password")
        document.getElementById('emailHelp').innerHTML = "Please enter email and password";
      }
    }
  }
}
</script>

<style>
  h1, small, p, img {
    animation: fadeInAnimation ease 3s;
    animation-iteration-count: 1; 
    animation-fill-mode: forwards;
  }
  @keyframes fadeInAnimation { 
    0% { 
      opacity: 0; 
    } 
    100% { 
      opacity: 1; 
     } 
  }
</style>