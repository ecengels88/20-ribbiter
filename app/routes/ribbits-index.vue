<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="profile-title">
          <h2 class="heading">Recent Ribblets</h2>
        </div>
        <div class="wrapper">
          <div class="card card__ribblet">
            <div class="new-ribblet">
              <div class="register__heading">
                <h1 class="register__title">New Ribblet</h1>
              </div>
              <form action="" class="form-inputs">
                <div class="input-padding">
                  <div class="input">
                    <p class="input__label">What's Going On?</p>
                    <textarea name="" id="" cols="30" rows="5" class="input__bar textarea"></textarea>
                  </div>
                </div>
                <div class="form-buttons">
                  <button class="btn login">Clear</button>
                  <button class="btn signup">Save</button>
                </div>
              </form>
            </div>
          </div>
          <div class="card card__all-ribblets">
            <div class="all-ribblets">
              <div class="register__heading">
                <h1 class="register__title">See What's Happening!</h1>
              </div>
              <div class="load-ribblets">
                <button class="btn load-btn">
                  Load New Ribblets
                </button>
              </div>
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
