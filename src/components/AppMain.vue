<script>
import AppMainBlueSection from "./AppMainBlueSection.vue";
import MainCard from "./MainCard.vue";

export default {
  data(){
    comicsCards: [
  {
    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
    "price": "$19.99",
    "series": "Action Comics",
    "type": "comic book"
  },
  {
    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
    "price": "$3.99",
    "series": "American Vampire 1976",
    "type": "comic book"
  },
  {
    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
    "price": "$16.99",
    "series": "Aquaman",
    "type": "graphic novel"
  },
  {
    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
    "price": "$2.99",
    "series": "Batgirl",
    "type": "comic book"
  },
  {
    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
    "price": "$3.99",
    "series": "Batman",
    "type": "comic book"
  },
  {
    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
    "price": "$2.99",
    "series": "Batman Beyond",
    "type": "comic book"
  },
  {
    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
    "price": "$3.99",
    "series": "Batman/Superman",
    "type": "comic book"
  },
  {
    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
    "price": "$4.99",
    "series": "Batman/Superman Annual",
    "type": "comic book"
  },
  {
    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
    "price": "$5.99",
    "series": "Batman: The Joker War Zone",
    "type": "comic book"
  },
  {
    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
    "price": "$6.99",
    "series": "Batman: Three Jokers",
    "type": "comic book"
  },
  {
    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
    "price": "$4.99",
    "series": "Batman: White Knight Presents: Harley Quinn",
    "type": "comic book"
  },
  {
    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
    "price": "$16.99",
    "series": "Catwoman",
    "type": "graphic novel"
  }
]
    
    return{

    }
  },
  components:{
    AppMainBlueSection,
    MainCard,
  }
}
</script>

<template>
    <div class="bg-black">
      <div id="main-img-bg"></div>
        <div class="my-container">
          <div id="current-series"> Current Series</div>
          <div id="cards-container">
            <MainCard></MainCard>
            <MainCard></MainCard>
            <MainCard></MainCard>
            <MainCard></MainCard>
            <MainCard></MainCard>
            <MainCard></MainCard>
            <MainCard></MainCard>
            <MainCard></MainCard>
          </div>
          <div>
            <button>Load More</button>
          </div>
        </div>
    </div>
    <AppMainBlueSection></AppMainBlueSection>
</template>

<style lang="scss" scoped>
    .bg-black{
        background-color: black;
        color: white;

        div{
            display: flex;
            align-items: center;
          }
          
          #main-img-bg{
            height: 350px;
            width: 100%;
            background-image: url("/img/jumbotron.jpg");
            background-size: cover;

          }

          .my-container{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;

            position: relative;
            padding: 1em 0;
            height: auto;


            #current-series{
              position: absolute;
              left: 0;
              top: -1em;

              background-color: dodgerblue;
              padding: 5px 1em;
              text-transform: uppercase;
            }

            #cards-container{
              display: flex;
              flex-flow: row wrap;
              justify-content: center;
              gap: 5px;

              padding: 2em 0;

              width: 100%;

              
            }

            button{
              background-color: dodgerblue;
              padding: 5px 3em;
              text-transform: uppercase;
              border: 1px solid white;
              font-weight: bold;
            }
          }
        }


</style>