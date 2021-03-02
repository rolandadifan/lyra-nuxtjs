<template>
<div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
    <div class="container">
    <b-container fluid>
      <nuxt-link to="/home" class="font text-center index-home"><h1>Lyra</h1></nuxt-link>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
                <nuxt-link to="/home">
                  <div class="index-home mr-3">
                    <i class="fas fa-home mr-2"></i>Home
                  </div>
                </nuxt-link>

                <nuxt-link to="/brows">
                  <div class="index-home">
                    <i class="fas fa-globe mr-2"></i>Brows
                  </div>
                </nuxt-link>
              <!-- <b-nav-item href="#" class="index-home"></b-nav-item> -->
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
 color: rgba(255, 255, 255, 0.5);

}
.index-home:hover{
  text-decoration: none;
  color: gray;
}
</style>