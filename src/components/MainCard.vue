<script>
    export default{
        data(){
            return{

            }
        },

        
        props: {
            cardTitle: String,
            cardImg: String,
        }
        
    }
</script>


<template>
    <div class="card">
        <div class="card-img">
            <img :src="cardImg" alt="img">
        </div>
        <div class="card-title"> {{ cardTitle }}</div>
    </div>
</template>

<style lang="scss" scoped>
    .card{
        display: flex;
        flex-direction: column;
        gap: 10px;

        margin-bottom: 0.5em;

        width: calc(100% / 6 - 10px);
        .card-img{
            width: 100%;
            height: 120px;

            overflow: hidden;

            img{
                width: 100%;
            
            }
        }

        .card-title{
            height: 3.5em;
            width:90%;
        }

    }


</style>