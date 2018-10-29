<template>
  <nav role="navigation" class="test">
    <a><router-link class="btn btn-primary" to="/" tag="button" alt="Home"><i class="fa fa-home"></i> Home</router-link></a>
    <a><router-link class="btn btn-primary" to="/about" tag="button" alt="About"><i class="fa fa-info-circle"></i> About</router-link></a>
  </nav>
</template>

<style media="screen">
.navbar-brand {
  position: float;
  width: 100%;
  left: 0;
  text-align: center;
  margin: 0 auto;
}
.navbar-toggle {
  z-index: 3;
}
</style>
