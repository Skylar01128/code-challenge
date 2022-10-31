<script setup>
    let props = defineProps({
        navLinks: {
            type: Array,
            required: true
        }
    })
</script>
<template>
    <div class="wrapper">
        <div class="nav-flex-group">
            <!-- ToDo -- Extract logo into separate component -->
            <a href=""><img src="../assets/images/Logo.png" alt=""></a>

            <ul id="navLinks">
                <li v-for="link in navLinks" :key="link">
                    <a href="#" class="font-semi-bold grey-text">{{link}}</a>
                </li>
            </ul>
        </div>

        <button id="free-trial" class="font-regular background-orange"> Free Trial</button>
    </div>
</template>

<style scoped lang="scss">

.wrapper{
    height: 72px;
    display: flex;
    flex-direction: row;
    margin-left: 11.5%;
    margin-right: 11.5%;
    align-items: center;
    justify-content: space-between;

    .nav-flex-group{
        display: flex;
        flex-direction: row;
        align-items: center;
    }
}
    #navLinks{
        list-style: none;
        display: flex;
        flex-direction: row;
        column-gap: 72px;
        margin: 0;
        padding-left: 91px;

        li{
            font-size: 16px;

            a{
                text-decoration: none;
            }
        }
    }

    #free-trial{
        width: 174px;
        height: 39px;
        border-radius: 0%;
        border: none;
        color: white;
        font-size: 15px;
    }

    #free-trial:hover{
        cursor: pointer;
    }
</style>