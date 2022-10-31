<script setup>

</script>

<template>
    <div id="banner" class="font-medium grey-text">
        
        <h4 class="font-medium grey-text">We're known for: </h4>

        <div id="products">

            <div>
                <img src="../assets/images/group.png" alt="">
                <h5 class="font-meduim">Leadership Development</h5>
            </div>
            <div>
                <img src="../assets/images/brackets.png" alt="">
                <h5 class="font-meduim">Technology <span>&#38;</span> Development</h5>
            </div>
            <div>
                <img src="../assets/images/clipboard.png" alt="">
                <h5 class="font-meduim">Compliance</h5>
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
    #banner{
        display: grid;
        justify-items: center;
        grid-template-rows: 1fr 1fr;

        h4{
            font-size: 36px;
            margin-top: 84px;
            margin-bottom: 35px;
        }

        #products{
            max-width: 1109px;
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;

            div{
                display: grid;
                grid-template-columns: 50% 50%;
                font-size: 20px;
                align-items: center;

                img{
                    display: grid; 
                    justify-self: flex-end;
                }

                h5{
                    text-transform: uppercase;
                    margin-left: 2rem;
                }
            }
        }
    }
</style>