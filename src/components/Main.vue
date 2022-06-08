<template>
    <main>
        <section>
            <p>Content goes Here</p>
        </section>

        <section id="shop">
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a :href="link.url"><img :src="link.img" alt=""><span>{{link.text}}</span></a>
                </li>
            </ul>
        </section>
    </main>
</template>

<script>
export default {
  name: 'MyMain',

    data(){
      return{
          links : [
                {
                text :"DIGITAL COMICS",
                url : "#",
                img : require("../assets/img/buy-comics-digital-comics.png")
              },

                {
                text :"DC MERCHANDISE",
                url : "#",
                img : require("../assets/img/buy-comics-merchandise.png")
              },

                {
                text :"SUBSCRIPRITION",
                url : "#",
                img : require("../assets/img/buy-comics-shop-locator.png")
              },

                {
                text :"COMIC SHOP LOCATOR",
                url : "#",
                img : require("../assets/img/buy-comics-subscriptions.png")
              },

                {
                text :"DC POWER VISA",
                url : "#",
                img : require("../assets/img/buy-dc-power-visa.svg")
              },

          ]
      }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
section{
    background-color: black;
    /* height: 150px; */
}

p{
    padding: 3% 14%;
    color: white;
    font-size: 25px;
}

#shop{
    background-color: rgb(4, 84, 158);

}

ul{
    padding: 3% 13%;
}

li{
    display: inline-block;
    list-style-type: none;
    margin: 0 15px;
}

a{
    color: white;
    text-decoration: none;
    display: flex;
    justify-content: space-around;
    align-items: center;
}

img{
    width: 65px;
    height: 75px;
    display: inline;
}
</style>