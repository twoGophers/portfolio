<template>
    <div class="v-hrLine">
        <hr>
        <h4 class="hrLine"
        @mouseover="mouseEnter"
        @mouseleave="mouseLeave"
        :style="styleRamk"
        >Обо мне</h4>
        <hr>
    </div>
</template>

<script>
export default {
    naem: "v-hrLine",
    data() {
        return {
            styleRamk : null
        }
    },
    methods: {
        mouseEnter() {
            this.styleRamk = `border-image:linear-gradient(45deg,white,black,white) 10;`;
        },
        mouseLeave() {
            this.styleRamk = `border-image:linear-gradient(45deg,black,white,black) 10;`;
        }
    },
}
</script>

<style lang="scss">
.v-hrLine{
    width: 100%;
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 1.5%;
    margin-bottom: 1.5%;
    hr {
    width: 40%;               
    border: 1px solid rgb(172, 172, 172);
    border-bottom-width: 0;
    }
    .hrLine{
        padding: 10px 15px;
        background: white;
        border: 3px solid;
        border-radius: 10px;
        border-image:linear-gradient(45deg,white,black,white) 10;
    }
}
</style>