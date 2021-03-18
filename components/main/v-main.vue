<template>
    <div class="v-main">

        <vHrLine />
        <vAboutMe />
    </div>
</template>

<script>
import vHrLine from "../componentCopy/v-hrLine"
import vAboutMe from "./v-aboutMe"

export default {
    name: "v-main",
    data() {
        return {
        }
    },
    components : {
        vHrLine,
        vAboutMe
    },

}
</script>

<style lang="scss">
.v-main{
    display: flex;
    flex-direction: column;
    .test{
        height: 500px;
    }
}
</style>