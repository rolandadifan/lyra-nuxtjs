<template>
    <footer>
        <b-card class="footer">
            <div class="row">
                <div class="col-2 text-center">
                    <h1 class="text-white">Lyra</h1>
                </div>
                <div class="col-2">
                    <h5>company</h5>
                    <nuxt-link class="footer-content" to="/about">About</nuxt-link> <br>
                    <a class="footer-content" href="#">Jobs</a> <br>
                    <a class="footer-content" href="#">For the Record</a>
                </div>
                <div class="col-2">
                     <h5>communities</h5>
                     <a class="footer-content" href="#">For Artist</a> <br>
                    <a class="footer-content" href="#">Developers</a> <br>
                    <a class="footer-content" href="#">Adversting</a> <br>
                    <a class="footer-content" href="#">Insverstor</a> <br>
                    <a class="footer-content" href="#">Vendors</a>
                </div>
                <div class="col-2">
                    <h5>useful links</h5>
                    <nuxt-link class="footer-content" to="/support">Support</nuxt-link> <br>
                    <a class="footer-content" href="#">Web Player</a>   
                </div>
                <div class="col-4">
                    <h5>Find Us</h5>
                    <div class="flex">
                        <a href="#">
                            <img class="footer-social-media mt-3"  src="~/assets/facebook.png" alt="">
                        </a>
                        <a href="#">
                            <img class="footer-social-media ml-3 mt-3" src="~/assets/instagram.png" alt="">
                        </a>
                    </div>
                </div>
            </div>
  </b-card>
    </footer>
</template>

<style scoped>
    .footer{
        background-color: #343a40;
        margin-top:-40px;
        height: 200px;
    }
    .footer-content{
        color: white;
        text-decoration: none;
    }
    .footer-content:hover{
        color: #02D608;
    }
    h5{
        color: black;
    }
    .footer-social-media{
        width: 50px;
    }
    .footer-social-media:hover{
        transform: translateY(-10px);
    }
</style>