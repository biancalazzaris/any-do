<template>
  <div class="head">
    <nav class="navbar navbar-light bg-dark mb-3">
      <div class="container-fluid">
        <a class="navbar-brand text-light" href="/">Any Do</a>
        <router-link class="navbar-brand text-light" to="/form">Hello {{name}} </router-link>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Head-menu',
};
</script>
<style>

</style>
