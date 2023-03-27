<script>
export default {
  data(){
    return{
        blueLinks:[
            {
                img: "/img/buy-comics-digital-comics.png",
                title: "Digital Comics",
            },
            {
                img: "/img/buy-comics-merchandise.png",
                title: "DC Merchandise",
            },
            {
                img: "/img/buy-comics-subscriptions.png",
                title: "Subscription",
            },
            {
                img: "/img/buy-comics-shop-locator.png",
                title: "Comic Shop Locator",
            },
            {
                img: "/img/buy-dc-power-visa.svg",
                title: "DC Power Visa",
            },
        ]
    }
  },
  
}
</script>

<template>
    <div class="bg-blue">
        <ul class="my-container">
            <li v-for="link in blueLinks">
                <div>
                    <img :src="link.img" alt="img">
                </div>
                <span> {{ link.title }}</span>
            </li>
        </ul>
    </div>

</template>

<style lang="scss" scoped>
    .bg-blue{
        background-color: dodgerblue;
        color: white; 

        ul{
            display: flex;
            flex-direction: row;
            justify-content: space-around;

            li{
                display: flex;
                flex-flow: row nowrap;
                justify-content: center;
                align-items: center;
                gap: 5px;
                font-size: 0.8em;
            }
        }
        
        div{
            height: 40px;
            max-width: 40px;

            img{
                width: 100%;
                height: 100%;
            }
        }

        span{
            text-transform: uppercase;
        }
    }
</style>