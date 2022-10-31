<script setup>

</script>

<template>
    <div id="footer-container">
        <div id="links-container">
            <div >
                <img src="../assets/images/Logo.png" alt="">
                <img src="../assets/images/social-media.png" alt="">
            </div>
            <div class="links company">
                <p class="font-bold bold-links">Company</p>
                <p class="font-light light-links">Leadership <br> Newsroom</p>
                <p class="font-light light-links"></p>
            </div>
            <div class="links">
                <p class="font-bold bold-links">Blog</p>
            </div>
            <div class="links">
                <p class="font-bold bold-links">Resources</p>

            </div>
            <div class="links">
                <p class="font-bold bold-links">Contect</p>

            </div>
        </div>

        <div>

        </div>
    </div>
</template>

<style scoped lang="scss">
    #footer-container{
        width: 1109px;
        height: 171px;
        display: grid;
        grid-template-rows: 80% 20%;
    }

    #links-container{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
    }

    p{
        font-size: 14px;
    }

    .links{
        display: grid;
        justify-items: center;
    }

    .light-links{
        font-size: 14px;
        margin: 0;
        height: fit-content;
    }

    .company{
        display: grid;
        height: fit-content;
        margin-bottom: 0;
    }
</style>