<template>
    <footer>
        <div class="container">
            <div class="spazio">
                <div id="comics">
                    <h2>DC COMICS</h2>
                    <ul>
                        <li v-for="(link, index) in links" :key="index">
                            <a :href="link.url"><span>{{link.text}}</span></a>
                        </li>
                    </ul>

                    <h2>SHOP</h2>
                    <ul>
                        <li v-for="(link, index) in shop" :key="index">
                            <a :href="link.url"><span>{{link.text}}</span></a>
                        </li>
                    </ul>
                </div>

                <div>
                    <h2>DC</h2>
                    <ul>
                        <li v-for="(link, index) in DC" :key="index">
                            <a :href="link.url"><span>{{link.text}}</span></a>
                        </li>
                    </ul>
                </div>

                <div>
                    <h2>SITES</h2>
                    <ul>
                        <li v-for="(link, index) in DC" :key="index">
                            <a :href="link.url"><span>{{link.text}}</span></a>
                        </li>
                    </ul>
                </div>

                <div id="dc_logo">
                </div>
            </div>
        </div>

        <!-- seconda parte footer -->
        <div id="seconda_parte">
            <a id="sign" href="#"><span>SIGN-UP NOW!</span></a>
            <div id="icon">
                <span><font color="blue">FOLLOW US</font></span>
                <a href="#"><img src="../assets/img/footer-facebook.png" alt="logo facebook"></a>
                <a href="#"><img src="../assets/img/footer-twitter.png" alt="logo twitter"></a>
                <a href="#"><img src="../assets/img/footer-youtube.png" alt="logo youtube"></a>
                <a href="#"><img src="../assets/img/footer-pinterest.png" alt="logo pinterest"></a>
                <a href="#"><img src="../assets/img/footer-periscope.png" alt="logo periscope"></a>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
  name: 'MyFooter',

data(){
      return{
          links : [
                {
                text :"Characters",
                url : "#",
              },

                {
                text :"Comics",
                url : "#",
              },

                {
                text :"Movies",
                url : "#",
              },

                {
                text :"TV",
                url : "#",
              },

                {
                text :"Games",
                url : "#",
              },
            {
                text :"Videos",
                url : "#",
              },
            {
                text :"News",
                url : "#",
              },

          ],

          shop : [
                {
                text :"Shop DC",
                url : "#",
              },

                {
                text :"Shop DC collectionables",
                url : "#",
              },
          ],

        DC : [
                {
                text :"Terms Of Use",
                url : "#",
              },

                {
                text :"Privacy policy (New)",
                url : "#",
              },
                {
                text :"Ad Choices",
                url : "#",
              },

                {
                text :"Advertising",
                url : "#",
              },
                {
                text :"Jobs",
                url : "#",
              },

                {
                text :"Subscriptions",
                url : "#",
              },
                {
                text :"Talent Workshops",
                url : "#",
              },

                {
                text :"CPSC Certificates",
                url : "#",
              },
                {
                text :"Ratings",
                url : "#",
              },

                {
                text :"Shop Help",
                url : "#",
              },
                {
                text :"Contact Us",
                url : "#",
              },
          ],
          sites : [
                {
                text :"DC",
                url : "#",
              },

                {
                text :"MAD Magazine",
                url : "#",
              },
            {
                text :"DC Kids",
                url : "#",
              },

                {
                text :"DC Universe",
                url : "#",
              },
                {
                text :"DC Power Visa",
                url : "#",
              },
          ]
      }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container{
    background-image: url("../assets/img/footer-bg.jpg");
    /* height: 650px; */
    background-size: 100%;
    background-repeat: no-repeat;
    
}

.spazio{
    display: flex;
    justify-content: flex-start;
    align-items: center;
    margin-left: 10%;
}

li{
    list-style: none;
}

h2{
    color: white;
    padding: 15px 50px;
}

ul{
    padding: 0 50px;
}

a{
    color: grey;
    text-decoration: none;
}

#comics{
    padding-top: 20px;
}

#dc_logo{
    background-image: url("../assets/img/dc-logo.png");
    background-size: 100%;
    background-position: center;
    width: 400px;
    height: 350px;
    background-repeat: no-repeat;
    opacity: 0.5;
    object-fit: cover;
    margin-left: 150px;
    transform: rotate(-0deg);
}

#seconda_parte{
    background-color: rgb(44, 43, 43);
    height: 100px;
    display: flex;
    justify-content: space-around;
    align-items: center;
}

#sign{
    color: white;
    border: 2px solid rgb(4, 84, 158);;
    padding: 15px;
}

#icon{
    display: flex;
    align-items: center;
}

img{
    margin: 10px;
}
</style>