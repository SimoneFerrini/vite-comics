<script>
    export default{
        data(){
            return{

            }
        }
    }
</script>


<template>
    <div class="card">
        <div class="card-img">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg" alt="img">
        </div>
        <div class="card-title">title</div>
    </div>
</template>

<style lang="scss" scoped>
    .card{
        display: flex;
        flex-direction: column;
        gap: 3px;

        width: calc(100% / 6 - 5 * 10px);
    }


</style>