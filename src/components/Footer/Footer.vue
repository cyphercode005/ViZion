
<template>
    <footer class="footer style-2">
        <div class="footer__top">
            <div class="container">
                <div class="row">
                    <div class="col-md-12">
                        <div class="content">
                            <h3 class="">{{title}}</h3>
                            <form action="#" id="subscribe-form1">
                                <input type="email" placeholder="Enter your email" required="" id="subscribe-email2" />
                                <button class="btn-action s2" type="submit" id="subscribe-button1"> <span class="effect">SUBSCRIBE TODAY</span></button>
                            </form>
                            <p>{{desc}}</p>
                            <!-- <ul class="list-social">
                                <li><span class="icon-twitter"></span></li>
                                <li><span class="icon-facebook"></span></li>
                                <li><span class="icon-place"></span></li>
                                <li><span class="icon-instagram"></span></li>
                                <li><span class="icon-reddit"></span></li>
                            </ul> -->
                            <ul class="list-social">
      <li><a href=" https://x.com/vizionprotocol" target="_blank" rel="noopener noreferrer"><span class="icon-twitter"></span></a></li>
      <li><a href="https://www.facebook.com/profile.php?id=61553090343551&mibextid=LQQJ4d" target="_blank" rel="noopener noreferrer"><span class="icon-facebook"></span></a></li>
      <li><a href="https://www.instagram.com/shanebrown360" target="_blank" rel="noopener noreferrer"><span class="icon-place"></span></a></li>
      <li><a href="https://www.instagram.com/shanebrown360" target="_blank" rel="noopener noreferrer"><span class="icon-instagram"></span></a></li>
      <li><a href="https://discord.com/invite/KaTVuF2TeW" target="_blank" rel="noopener noreferrer"><span class="icon-reddit"></span></a></li>
    </ul>

                        </div>
                    </div>
                    <div class="col-md-5">
                        
                    </div>
                </div>
            </div>
        </div>
        <div class="footer__bottom center">
            <div class="container">
                <div class="row">
                    <div class="col-md-12">
                        <p>© 2022. All rights reserved by <router-link to="/">{{author}}</router-link></p>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>

import "./styles.scss";

export default {
    name: "Feature",
     data (){
        return {
            
            title: "Don't miss out, Stay updated",
            desc: 'Don’t hesitate to subscribe to latest news about ViZion Protocol!',
            author:'ViZion Protocol'
        }    
    }
};
</script>
            
            