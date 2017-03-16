<template lang="html">
  <div class="app">
    <nav class="nav">
      <div class="nav-left">
        <a href="/" class="nav-item">
          <p>Ribbiter</p>
        </a>
      </div>
      <div class="nav-right">
        <a href="" class="nav-item">
          <p>Ribblets</p>
        </a>
        <a href="" class="nav-item">
          <p>Frogs</p>
        </a>
        <a href="" class="nav-item">
          <p>Login</p>
        </a>
      </div>
    </nav>
    <div class="section">
      <div class="container">
        <router-view></router-view>
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
