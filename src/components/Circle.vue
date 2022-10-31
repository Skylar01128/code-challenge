<script setup>
const props = defineProps({
    image: String,
    text: String,
})

</script>

<template>
    <div id="wrapper">
        <div class="circle-text">
            <div class="circle magenta">
                <img :src="props.image" alt="" />
            </div>
            <h5 class="font-medium grey-text">{{text}}</h5>
        </div>

    </div>
</template>

<style>
    .circle{
        width: 92px;
        height: 92px;
        border-radius: 50%;
        display: grid;
        justify-content: center;
        align-content: center;
    }

    .circle-text{
        display: grid;
        justify-items: center;
    }

    #wrapper{
        display: grid;
    }

    .book img{
        padding-left: 10px;
    }
</style>