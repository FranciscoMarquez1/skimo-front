<template>
    <b-navbar toggleable="lg" type="dark" variant="info" fixed class="navbar">
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

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
.navbar {
    width: 100%;
    background-color: #005418 !important;
}

</style>