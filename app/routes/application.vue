<template lang="html">
  <div class="app">
    <nav class="nav">
      <div class="left">
        <p class="left__nav-item">
          <a href="/">Ribbiter</a>
        </p>
      </div>
      <div class="right">
        <p class="right__nav-item">
          <a href="">Ribblets</a>
        </p>
        <p class="right__nav-item">
          <a href="/users" class="nav-item">Frogs</a>
        </p>
        <p class="right__nav-item">
          <a href="/login" class="nav-item">Login</a>
        </p>
      </div>
    </nav>
    <router-view></router-view>
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
