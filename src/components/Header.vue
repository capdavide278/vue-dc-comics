<template>
    <header>
        <div class="container">
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="logo dc comics">
            </a>

            <div class="space-left">
                <nav>
                    <ul>
                        <li v-for="(link, index) in links" :key="index">
                            <a id="bordo" :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
export default {
  name: 'myHeader',
  data(){
      return{
          links : [
              {
                text :"CHARACTERS",
                url : "#"
              },

            {
                text :"COMICS",
                url : "#"
            },
             {
                text :"MOVIES",
                url : "#"
              },

                {
                text :"TV",
                url : "#"
              },

                {
                text :"GAMES",
                url : "#"
              },

                {
                text :"COLLECTIBILES",
                url : "#"
              },

                {
                text :"VIDEOS",
                url : "#"
              },

                {
                text :"FANS",
                url : "#"
              },

                {
                text :"NEWS",
                url : "#"
              },

                {
                text :"SHOP",
                url : "#"
              },

          ]
      }

  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
    margin-top: 2%;
}

.container{
    display: flex;
    justify-content: space-around;
    align-items: center;
}

li{
    display: inline;
    list-style-type: none;
    margin-left: 2%;
}

.space-left{
    margin-right: 10%;
}

#bordo{
    color: black;
    text-decoration: none;
}

#bordo:hover{
    color: rgb(14, 17, 214);
    border-bottom: 3px solid blue;
    padding-bottom: 42px;
}

</style>