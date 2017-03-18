<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="card">

          <div class="register">
            <!-- Give this no padding and bg -->
            <div class="register__heading">
              <h1 class="register__title">Create an Account</h1>
            </div>

            <form action="" class="form-inputs">
              <div class="input">
                <p class="input__label">Username</p>
                <input type="text" class="input__bar username" placeholder="Username" v-model="username">
                <p>{{}}</p>
              </div>
              <div class="input">
                <p class="input__label">Email</p>
                <input type="text" class="input__bar email" placeholder="Email" v-model="email">
              </div>
              <div class="input">
                <p class="input__label">Password</p>
                <input type="password" class="input__bar password" placeholder="Password" v-model="password">
              </div>
            </form>
            <div class="form-buttons">
              <button class="btn login">Login</button>
              <button class="btn signup">Sign Up</button>
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
    };
  },

  methods: {

  },
};
</script>
