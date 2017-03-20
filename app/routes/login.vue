<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="card">

          <div class="register">
            <!-- Give this no padding and bg -->
            <div class="register__heading">
              <h1 class="register__title">Login</h1>
            </div>

            <form action="" class="form-inputs">
              <div class="input-padding">
                <div class="input">
                  <p class="input__label">Email</p>
                  <input type="text" class="input__bar email" placeholder="Email" >
                </div>
                <div class="input">
                  <p class="input__label">Password</p>
                  <input type="password" class="input__bar password" placeholder="Password" >
                </div>
              </div>
            <div class="form-buttons">
              <button class="btn signup">Register</button>
              <button class="btn login">Login</button>
            </div>
          </form>
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
