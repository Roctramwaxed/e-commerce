<template>
  <div>
    <div class="container d-flex justify-content-center form-group">
      <form>
        <div class="card" style="width: 32rem;">
          <div class="card-body">
            <h5 class="card-title">Become a hero now!</h5>
            <div class="row mt-5 mx-auto justify-content-center">
              <label class="col-3 justify-content-">Email</label>
              <input class="col-8" type="email" v-model="email">
            </div>
            <div class="row mt-3 mx-auto justify-content-center">
              <label class="col-3 justify-content-">Password</label>
              <input class="col-8" type="password" v-model="password">
            </div>
            <!-- <input class="btn btn-primary" type="submit" value="Login"> -->
            <a class="btn btn-primary mt-5" @click.prevent="register">Register</a>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    register () {
      this.$store.dispatch('register', {email: this.email, password: this.password})
    }
  }
}
</script>

<style>

</style>