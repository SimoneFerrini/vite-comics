<script>
import AppMainBlueSection from "./AppMainBlueSection.vue";

export default {
  data(){
    return{

    }
  },
  components:{
    AppMainBlueSection,
  }
}
</script>

<template>
    <div class="bg-black">
        <div class="my-container">
             <h2>
                --&gt; Content goes here &lt;--
            </h2>
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
    }
</style>