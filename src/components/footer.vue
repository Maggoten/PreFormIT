<template >
    <footer class="test">
        <p>Partners</p>
        <a v-for="image in images" :href="image.href">
          <img :src="(image.src)" :class="imgpartner" :alt="image.alt" :title="image.title"/>
        </a>
    </footer>
</template>

<script>


export default{
    data(){
        return{
            images: [
            {name:"Adobe", href:"https://www.adobe.com", src:require('../assets/img/adobe-logo.png'), alt:"Adobe logo", title:"Adobe" },
            {name:"Microsoft", href:"https://www.microsoft.com", src:require('../assets/img/MicrosoftPartnerLogo.jpg'), alt:"Microsoft", title:"Microsoft"}]
        }
    },
    methods:{

    }
}
</script>


<style>

</style>
