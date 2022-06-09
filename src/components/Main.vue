<template>
    <main>
        <section>
            <div id="jumbo"></div>
            <div id="serie">
                <a href="#"><h2>CURRENT SERIES</h2></a>
            </div>
        </section>
        <section>
            <div id="in_vista">
                <ul>
                    <li v-for="(element, i) in merce" :key="i">
                        <a><img :src="element.thumb" alt="">
                        <div>{{element.series}}</div></a>
                    </li>
                </ul>
            </div>

        <div id="read_more">
            <a id="load_more" href="#"><p>LOAD MORE</p></a>
        </div>
        </section>

        <section id="shop">
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a id="options" :href="link.url"><img :src="link.img" alt=""><span>{{link.text}}</span></a>
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
    },
    props:{
        merce: Array,
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#serie{
    width: 300px;
    padding: 30px;
    margin-left: 250px;
    background-color:rgb(4, 84, 158) ;
    object-position: 25% 75%;
    a{
        color: white;
        text-decoration: none;
    }
}


#jumbo{
    background-image: url("../assets/img/jumbotron.jpg");
    height: 410px;
}

section{
    background-color: rgb(37, 37, 37);
    /* height: 150px; */
}

#in_vista{
    display: flex;
    justify-content: center;


    img{
        height: 220px;
        width: 200px;
        padding-bottom: 20px;
    }
    div{
        /* padding: 3% 14%; */
        color: white;
        /* font-size: 15px; */
        max-width: 200px;
    }

    li{
        margin: 15px;
        margin-bottom: 20px;
        display: inline-block;
    }

    ul{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
}

#read_more{
    display: flex;
    justify-content: center;
    align-items: center;

    a{
    background-color: rgb(4, 84, 158);
    margin-bottom: 20px;
    padding: 15px;
    width: 15%;
    color: white;
    text-decoration:none;
    }

    p{
        text-align: center;
    }
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

#options{
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