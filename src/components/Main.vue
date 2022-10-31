<script setup>
    import Hero from "./Hero.vue"
    import Banner from "./Banner.vue"
    import ImageGrid from "./ImageGrid.vue"
    import Learn from "./Learn.vue"
</script>

<template>

    <section id="hero">
        <Hero />
    </section>

    <section>
        <Banner />
    </section>

    <section id="image-grid">
        <ImageGrid />
    </section>

    <section id="learn" class="cream">
        <Learn />
    </section>
    
</template>

<style scoped lang="scss">
    #hero{
        height: 681px;
        width: 100%;
        background-image: url("../assets/images/hero.png");
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        background-position-x: -41px
    }

    #image-grid{
        display: grid;
        justify-content: center;
    }

    #learn{
        width: 100%;
        height: 265px;
        margin-top: 30px;
        display: grid;
        justify-content: center;
    }
</style>