<script setup>
import {ref, reactive, onMounted} from "vue"
const props = defineProps({
        image: {
            type: Object,
            required: true,
            default: {location: "/src/assets/images/smile.png", id: "smile", header: "Leadership Development", text: "Leading with Vision"}
        }
    })

    
    const hover = ref(false)
    const objHeight = props.image.height
    // const height = ref('113px')

    const height = reactive({ height: "113px" })
    const parent = reactive({height: props.image.parentHeight})

 
    

</script>


<script setup>
</script>

<template>
    <div :class="props.image.id" class="image">
        <div class="img-text " :class="props.image.color" :style="{height: height.height}" @mouseenter="height.height = parent.height" @mouseleave="height.height = props.image.height">
            <h6 class="font-bold uppercase">{{props.image.header}}</h6>
            <p class="font-bold">{{props.image.text}}</p>
        </div>

    </div>
</template>

<style scoped lang="scss">

    .image{
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        display: grid;
        align-content: flex-end;
    }

    .smile{
        background-image: url("../assets/images/smile.png");
            
    }

    .vr{
        background-image: url("../assets/images/vr.png");
            
    }

    .review{
        background-image: url("../assets/images/review.png");
        .img-text{
            width: 99%;
        }
            
    }

    .whiteboard{
        background-image: url("../assets/images/whiteboard.png");
        .img-text{
            width: 99%;
        }
            
    }

    .politics{
        background-image: url("../assets/images/politics.png");
            
    }

    
    .meeting{
        background-image: url("../assets/images/meeting.png");

        .img-text{
            width: 99%;
        }
            
    }

    h6{
        color: white;
        font-size: 24px;
        width: 206px;
    
        margin: 0;
    }

    .img-text{
        height: 113px;
        display: grid;
        align-content: flex-end;
        padding-left: 2rem;
        width: 100%;
        justify-self: center;
        padding-bottom: 1em;
        transition: height 200ms ease-in-out;
       
    }

    p{
        margin: 0;
        font-size: 20px;
    }

</style>