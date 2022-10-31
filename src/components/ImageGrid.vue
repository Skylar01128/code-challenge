<script setup>
import GridImage from "./GridImage.vue"
const images = [
    {location: "/src/assets/images/smile.png", id: "smile", color: 'magenta', header: "Leadership Development", text: "Leading with Vision", height: "113px", parentHeight: "738px"}, //Not how I would choose to do this normally, but sometimes you have to improvise when on a time crunch!
    {location: "/src/assets/images/smile.png", id: "vr", color: 'orange', header: "TECHNOLOGY & DEVELOPMENT", text: "Developer", height: "111px", parentHeight: "366px"},
    {location: "/src/assets/images/smile.png", id: "review", color: 'yellow',header: "COMPLIANCE ", text: "Leading with Vision", height: "107px", parentHeight: "366px"},
    {location: "/src/assets/images/smile.png", id: "meeting", color: 'orange', header: "TECHNOLOGY & DEVELOPMENT", text: "Security", height: "113px", parentHeight: "242px"},
    {location: "/src/assets/images/smile.png", id: "whiteboard", color: 'yellow',header: "Leadership Development", text: "Management Essentials", height: "112px", parentHeight: "242px"},
    {location: "/src/assets/images/smile.png", id: "politics", color: 'magenta', header: "COMPLIANCE ", text: "Compliance Training for the Federal Government", height: "107px", parentHeight: "242px"}]

function imageToShow(parentIndex,childIndex) {
    let image = '';
    if(parentIndex == 1){
        image = images[0]
    }else if(parentIndex == 2){
        if(childIndex == 1){
            image = images[1]
        }else{
            image = images[2]
        }
    }else{
        if(childIndex == 1){
            image = images[3]
        }else if(childIndex == 2){
            image = images[4]
        }else{
            image = images[5]
        }
    }

    return image
};

function rowClass(iterator) {
    let rowClass = '';
    if(iterator == 1){
        rowClass = "row-1"
    }else if(iterator == 2){
        rowClass = "row-2"
    }else{
        rowClass = "row-3"
    }

    return rowClass
};

</script>

<template>
    <div id="grid">
        <!-- create 3 columns -->
        <div v-for="i in 3" :key="i" class="col" :class="rowClass(i)">
            <!-- Create the necessary amount of GridImage elements for each column and pass the image object as a prop -->
                <GridImage v-for="j in i" :key="j" :image="imageToShow(i,j)">
         </GridImage>
        </div>

    </div>
</template>

<style scoped lang="scss">
    #grid{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        height: 738px;
        width: 1109px;
        grid-column-gap: 5px;

        .col{
            display: grid;
            grid-row-gap: 5px;
            grid-column-gap: 5px;
        }

        .row-2{
            grid-template-rows: 1fr 1fr;
        }

        .row-3{
            grid-template-rows: 1fr 1fr 1fr;
        }

    }
</style>