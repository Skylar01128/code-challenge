<script setup>
    import Circle from "./Circle.vue"
    const images = ['phone', 'book', 'laptop']
</script>

<template>
    <div class="inner">
        <h4 class="font-medium grey-text inner-title">Ways you can learn</h4>

        <div id="icon-container">
            <Circle image="/src/assets/images/phone.png" text="MOBILE DEVICES" class="flex-end phone"/>
            <Circle image="/src/assets/images/book.png" text="EBOOKS" class="book"/>
            <Circle image="/src/assets/images/laptop.png" text="LIVE LEARNING" class="flex-start laptop"/>
        </div>
    </div>
</template>


<style scoped lang="scss">
.inner {
    width: 1109px;
    display: grid;

    .inner-title{
        margin-top: 30px;
        display: grid;
        justify-content: center;
    }

    h4{
        margin: 0;
        font-size: 36px;
    }

    #icon-container{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
    }

    .flex-end{
        display: grid; 
        justify-content: flex-end;
    }

    .flex-start{
        display: grid; 
        justify-content: flex-start;
    }
}
</style>