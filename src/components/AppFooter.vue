<script>
    export default {
    data(){
        return{
            footerElements:[
                {
                    title: "DC Comics",
                    footerLinks:["Characters",
                                 "Comics",
                                 "Movies",
                                 "TV",
                                 "Games",
                                 "Videos",
                                 "News",
                    ],
                },
                {
                    title: "DC",
                    footerLinks:["Term of use",
                                 "Privacy policy (New)",
                                 "Ad Choices",
                                 "Advertising",
                                 "Jobs",
                                 "Subscriptions",
                                 "Talent Workshops",
                                 "CPSC Certificates",
                                 "Ratings",
                                 "Shop Help",
                                 "Contact Us",
                    ],
                },
                {
                    title: "Sites",
                    footerLinks:["DC",
                                 "Mad Magazine",
                                 "DC Kids",
                                 "DC Universe",
                                 "DC Power Visa",
                    ],
                },{
                    title: "Shop",
                    footerLinks:["Shop DC",
                                 "Shop DC Collectibles"
                    ],
                }
            ],

            footerBottomIcons:[
                "/img/footer-facebook.png",
                "/img/footer-twitter.png",
                "/img/footer-youtube.png",
                "/img/footer-pinterest.png",
                "/img/footer-periscope.png",
            ]
            
        }
    }
}
</script>

<template>
    <div class="bg-footer">
        <div class="footer my-container">
             <div class="footer-left">
                 <ul class="list-elem-container">
                     <li v-for="element in footerElements" class="list-elem">
                        <span class="link-title"> {{ element.title }} </span>
                         <ul>
                             <li v-for="link in element.footerLinks" class="list-link">
                                 {{ link }}
                             </li>
                         </ul>
                     </li>
                 </ul>
             </div>
         
             <div class="footer-right">
                 <img src="/img/dc-logo-bg.png" alt="logo">
             </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="my-container">
            <div class="footer-b-left">
            <button> Sign-Up Now</button>
        </div>
        <div class="footer-b-right">
            <span> Follow Us</span>
            <ul>
                <li v-for="icon in footerBottomIcons">
                    <img :src="icon" alt="icon">
                </li>
            </ul>
        </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
    .bg-footer{
        background-image: url("/img/footer-bg.jpg");
        background-size: cover;
        height: 400px;
    }

    
    .footer{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
       
        height: 100%;

        
    }
    .footer-left{

        display: flex;
        width: 40%;
        height: 100%;
        padding: 2em 0;
    }

    ul.list-elem-container{
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            flex-wrap: wrap;
            height: 100%;          
            

        }

    li.list-elem{
        display: flex;
        flex-direction: column;
        
        width: 30%;
        margin-bottom: 1em;
               
    }
    .link-title{
        text-transform: uppercase;
        font-size: 1.2em;
        margin-bottom: 1em;
    }
    li.list-link{
        font-size: 0.6em;
    }

        
                
    .footer-right{
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        width: 60%;
    
        img{
            width: 100%;
        };
    }    

    
    .footer-bottom{
        background-color: rgb(40, 40, 40);
        
        .my-container{
            display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        
        }
    }
    .footer-b-left{
        button{
            padding: 1em;
            text-transform: uppercase;
            background-color: transparent;
            color: white;
            border: 1px solid dodgerblue;
        }
    }

    
    .footer-b-right{
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 1em;

        span{
            text-transform: uppercase;
            color: dodgerblue;
            font-weight: 600;
        }

        ul{
            display: flex;
            flex-direction: row;
            gap: 1em;
        }
    }

    
</style>