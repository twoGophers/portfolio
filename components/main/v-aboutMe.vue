<template>
    <div class="v-aboutMe">

        <div class="fotoUser">
            <div class="fotoUser-item">
                <img 
                :src="require('@/assets/images/sm.jpg')" alt="" srcset=""
                @mouseover="mouseEnter"
                @mouseleave="mouseLeave"
                :style="styleRamk"
                >
            </div>
            <div class="fotoUser-name">
                <h4
                @mouseover="mouseEnter"
                @mouseleave="mouseLeave"
                :style="styleRamk1"
                >Web programmer</h4>
            </div>
        </div>

        <div class="infoUser">
            <vAboutMeMain />
        </div>
    </div>
</template>

<script>
import vAboutMeMain from "./v-aboutMeMain"

export default {
    name: "v-aboutMe",
    data() {
        return {
            styleRamk : null,
            styleRamk1 : null
        }
    },
    components : {
        vAboutMeMain
    },
    methods: {
        mouseEnter() {
            this.styleRamk = 'border : 3px solid rgb(221, 221, 221)', `transition-delay: 3s;`;
            this.styleRamk1 = `color : rgb(161, 161, 161)`, `transition-delay: 3s;`;
        },
        mouseLeave() {
            this.styleRamk = 'border : 3px solid white', `transition-delay: 3s;`;
            this.styleRamk1 = `color : rgb(92, 91, 91)`, `transition-delay: 3s;`;
        }
    },
}
</script>

<style lang="scss">
.v-aboutMe {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    .fotoUser{
        width: 20%;
        display: flex;
        justify-items: center;
        flex-direction: column;
        padding-left: 3%;
        padding-right: 3%;
        .fotoUser-item{
            border: 1px solid rgb(139, 139, 139);
            width: 100%;
            background: white;
            transition: 0.5s ease;
            display: flex;
            img {
                width: 100%;
                border: 3px solid white;
                transition: 0.5s ease;
            }
        }
        .fotoUser-name{
            margin-top: 10%;
            display: flex;
            justify-content: center;
            transition: 0.5s ease;
            h4{
                color: rgb(92, 91, 91);
                transition: 0.5s ease;
            }
        }
    }
    .infoUser{
        width: 70%;
        padding-left: 5%;
    }
}
</style>