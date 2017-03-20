<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="profile-title">
          <h2 class="heading">Frogs</h2>
        </div>
        <div class="profile">
          <div class="profile__item" v-for="users in users.items">
            <div class="card">
              <div class="card__image">
                <img src="http://www.placecage.com/140/100" alt="" class="card-pic">
              </div>
              <div class="card__id">
                <p class="name">{{ users.username }}</p>
                <p class="user-id">{{ users.email }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import store from '../store';
import userResource from '../resources/user';

export default {
  data() {
    return {
      users: this.$select('users'),
    };
  },

  created() {
    const { actionCreators: { findAll } } =  userResource;
    store.dispatch(findAll());
  },

  methods: {
  },
};
</script>
