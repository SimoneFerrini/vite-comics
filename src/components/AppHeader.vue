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
        ],

        activeIndex: 0,
    }
  },

  methods:{
    setIndex(index){
        this.activeIndex = index;
    }
  }
}
</script>

<template>
    <div class="header">
        <div class="header-container my-container">
            
            <div class="logo">
                <img src="/img/dc-logo.png" alt="img">
            </div>
            <ul>
                <li v-for="(link,index) in linksHeader" @click="setIndex(index)" :class="activeIndex == index ? 'active' : ' ' ">{{ link }} </li>
                
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
            height: 100%;

            li{
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100%;
                padding: 0.8em;
                text-transform: uppercase;
                font-weight: 600 ;
                border-bottom: 4px solid transparent;
                
                &.active{
                    color: dodgerblue;
                    border-bottom: 4px solid dodgerblue;
                }
            }

            
        }
    };
    

    
  

</style>