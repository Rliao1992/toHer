<template>
    <q-layout>
        <div class="layout-view">
            <!--<div class="logo-container non-selectable no-pointer-events">
                <div class="logo">
                    <p class="caption text-center">
                        <span>有话对她说</span>
                    </p>
                </div>
            </div>-->
        </div>
    </q-layout>
</template>
<style lang="stylus" scoped>
    @import '~themes/app.variables'
    .layout-view{
        // display: block;
        // background-image: url("~assets/public/background.jpg");
        // background-size: cover;
        // background-repeat: no-repeat;
        // background-position: center center;
        // background-attachment: fixed;
        background-color: #fff; 
        background-image: 
        linear-gradient(90deg, transparent 79px, #abced4 0px, #abced4 0px, transparent 81px),
        linear-gradient(#eee .1em, transparent .1em);
        background-size: 100% 1.2em;
    }
    .logo{
        width: 240px;
        height: 240px;
        background-image: url("~assets/public/heart.png");
        background-size: cover;
        margin-left: auto;
        margin-right: auto;
        margin-top: 50%;
        margin-bottom: 50%;
    }

    .logo > .caption{
        font-size: 18px;
        line-height: 240px;
        color: #fff;
        font-weight: bold;
    }
</style>