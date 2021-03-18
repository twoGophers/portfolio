<template>
    <div class="v-infoUser">
        <div class="infoUser">
            <p class="nameStyle">Владимир</p>
            <p>Возраст : 27 лет</p>
            <p>Frontend - разработчик</p>
            <p style="margin-top:5%">Обо мне : 
                <span>
                Занимаюсь разработкой одностраничных сайтов под ключ. 
                По возможности изучаю английский язык и новые введение в веб-разработке, практикуя знания на практике.
                Делаю резиновую, адаптивную верску Flex под мобильные устройства и планшеты.
                </span>
            </p>
        </div>
        
        <div class="steck">
            <p>HTML : 1.5 года</p>
            <p>PUG : 2 мес</p>
            <p>CSS : 1.5 года</p>
            <p>SCSS : 1 год</p>
            <p>Bootstrap, Vuetify : 7 мес</p>
            <p>Java Script : 7 мес</p>
            <p>Vue 2.0 : 5 мес</p>
            <p>Nuxt : 2 мес</p>
            <p>Php : 2 мес</p>
            <p>Git : 1 год</p>
        </div>

    </div>
</template>
<script>
export default {
    name: "v-infoUser"
}
</script>

<style lang="scss">
.v-infoUser{
    border-radius: 20px;
    width: 90%;
    display: flex;
    padding: 2%;
    background-color:rgba(0,0,0,.3);
    p{
        line-height: 1.7em;
        background-image:linear-gradient(
            to bottom,
            rgb(250, 248, 248) 0%,
            rgb(201, 201, 202) 100%
        );
        background-clip:text;
        --webkit-background-clip:text;
        color:transparent;
    }
    .infoUser{
        width: 60%;
        .nameStyle{
            font-size: 1.5em;
        }
    }
    .steck{
        width: 40%;
        margin-left: 15%;
    
    }
}
</style>