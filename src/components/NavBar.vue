<template>
    <b-navbar toggleable="lg" variant="info" fixed class="navbar-custom">
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <div class="arrow-up"></div>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">Skimo</b-nav-item>
          <b-nav-item href="#">Menú</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
            <b-nav-item href="#">Contacto</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
.navbar-custom {
    width: 100%;
    padding: 1.5rem;
    background-color: #005418 !important;
}
.navbar-custom a {
    color: #ffffff !important;
    font-size: 1.5rem;
}

.arrow-up {
  width: 0; 
  height: 0; 
  border-left: 30px solid transparent;
  border-right: 30px solid transparent;
  border-bottom: 50px solid #00944d;
  margin-left: 20px;
}

</style>