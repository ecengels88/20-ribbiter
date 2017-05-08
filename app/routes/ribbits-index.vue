<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="profile-title">
          <h2 class="heading">Recent Ribblets</h2>
        </div>
        <div class="grid">
          <div class="grid__item grid__item--left">
            <div class="card">
              <div class="new-ribblet">
                <div class="register__heading">
                  <h1 class="register__title">New Ribblet</h1>
                </div>
                <form action="" class="form-inputs" v-on:submit.prevent="create(formValues)">
                  <div class="input-padding">
                    <div class="input">
                      <p class="input__label">What's Going On?</p>
                      <textarea name="" id="" cols="30" rows="5" class="input__bar textarea" v-model="formValues.body"></textarea>
                    </div>
                  </div>
                  <div class="form-buttons">
                    <button class="btn login">Clear</button>
                    <button class="btn signup">Save</button>
                  </div>
                </form>
              </div>
            </div>
          </div>
          <div class="grid__item grid__item--right">
            <div class="card">
              <div class="all-ribblets">
                <div class="register__heading">
                  <h1 class="register__title">See What's Happening!</h1>
                </div>
                <div class="load-ribblets">
                  <button class="btn load-btn">
                    Load New Ribblets
                  </button>
                </div>
                <div class="ribblets" v-for="post in posts.items">
                  <div class="ribblets__item">
                    <p class="user-id user-id__tweets">{{post.user.username}}</p>
                    <p class="user-tweets">{{post.body}}</p>
                  </div>
                </div>
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
import postResource from '../resources/post';
const create = postResource.actionCreators.create;

export default {
  data() {
    return {
      posts: this.$select('posts'),
      formValues: {
        body: '',
      }
    };
  },

  mounted() {
    const { actionCreators: { findAll } } =  postResource;
    store.dispatch(findAll());
  },

  methods: {
    create(formValues) {
      store.dispatch(create(formValues))
        .then(() => {
          this.clear();
        }).catch(() => {});
    },

    clear() {
      this.formValues = {
        body: '',
      };
    }
  },
};
</script>
