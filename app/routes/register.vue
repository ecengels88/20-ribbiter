<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">

        <div v-if="users.loading === 'error'" class="alert alert-danger">
          <h2>There was an error creating this user</h2>
        </div>

        <div class="card">

          <div class="register">
            <!-- Give this no padding and bg -->
            <div class="register__heading">
              <h1 class="register__title">Create an Account</h1>
            </div>

            <form action="" class="form-inputs" v-on:submit.prevent="create(formValues)">
              <div class="input-padding">
                <div class="input">
                  <p class="input__label">Username</p>
                  <input type="text" class="input__bar username" placeholder="Username" v-model="formValues.username">
                </div>
                <div class="input">
                  <p class="input__label">Email</p>
                  <input type="text" class="input__bar email" placeholder="Email" v-model="formValues.email">
                </div>
                <div class="input">
                  <p class="input__label">Password</p>
                  <input type="password" class="input__bar password" placeholder="Password" v-model="formValues.password">
                </div>
              </div>
              <div class="form-buttons">
                <button class="btn login">Login</button>
                <button class="btn signup">Register</button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import store from '../store';
import createResource from '../resources/user';
const create = createResource.actionCreators.create;

export default {
  data() {
    return {
      users: this.$select('users'),
      formValues: {
        username: '',
        email: '',
        password: '',
      }
    };
  },

  methods: {
    create(formValues) {
      store.dispatch(create(formValues))
        .then(() => {
          this.$router.push({ name: 'users' });
        }).catch(() => {});
    },
  },
};
</script>
