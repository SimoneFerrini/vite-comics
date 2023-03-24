<script>
export default {
  data(){
    return{
        linksHeader:[
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Collectibles",
            "Videos",
            "Fans",
            "News",
            "Shop"
        ]
    }
  }
}
</script>

<template>
    <div class="header">
        <div class="header-container">
            
            <div class="logo">
                <img src="/img/dc-logo.png" alt="img">
            </div>
            <ul>
                <li v-for="link in linksHeader">{{ link }} </li>
                
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .header{
        width: 100%;
        background-color: white;

        .header-container{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        
        max-width: 70%;
        margin: 0 auto;

            .logo{
                width: 70px;
                margin: 1em 0;

                img{
                    width: 100%;
                }
            }
        
        }

        ul{
            display: flex;
            flex-direction: row;
            
            color: black;
            font-size: 0.8em;

            li{
                height: 100%;
                padding: 0.8em;
                text-transform: uppercase;
                font-weight: 600 ;
            }
            
        }
    }

  

</style>