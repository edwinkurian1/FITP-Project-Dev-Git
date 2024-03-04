<template>
  <div class="row background_border">
  <div class="container">
   
    <div class="row justify-content-center mt-5">
      <div class="col-md-6">
        <div class="card">
          <div class="card-header">Member Login</div>
          <div class="card-body">
            <form @submit.prevent="login">
              <div class="form-group">
                <label for="email">Email address</label>
                <input type="email" class="form-control" id="email" v-model="email" required>
              </div>
              <div class="form-group">
                <label for="password">Password</label>
                <input type="password" class="form-control" id="password" v-model="password" required>
              </div>
              <button type="submit" class="btn btn-primary">Login</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: ''
    };
  },
  methods: {
    login() {
      // Here you can implement your login logic
      console.log('Email:', this.email);
      console.log('Password:', this.password);
      // You may use Axios or Vue Resource to send login request to your server
    }
  }
};
</script>

<style>
.container {
  margin-top: 30px;
  border-radius: 10px;
}
.background_border {
    /* background-color:; */
    background-origin: content-box;
    /* margin-top: 3% !important; */
    padding-top: 1% !important;
    height: 582px;
    background: url("..\assets\image\background.jpg")  no-repeat center center fixed #000; 
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
}
</style>
