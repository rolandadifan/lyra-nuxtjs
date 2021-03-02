<template>
<div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
    <div class="container">
    <b-container fluid>
      <b-navbar-brand href="#" class="font text-center index-home"><h1>Lyra</h1></b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
              <b-nav-item href="#" class="index-home">Premium</b-nav-item>
              <b-nav-item href="#" class="index-home">Support</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
    </b-container>
    </div>
  </b-navbar>
</div>
</template>

<style scoped>
.index-home {
  font-size: 24px; 
}



</style>