<template>
<div class="app">
  <vHeader />
  <vMain />
  <div class="test">
    <p>{{this.scrollPosition}}</p>
  </div>
  <div class="test" style="height:1000px"></div>
</div>
</template>

<script>

import vHeader from "../components/header/v-header"
import vMain from "../components/main/v-main"

export default {
  name: 'app',
  components : {
    vHeader,
    vMain
  },
  data () {
      return {
        scrollPosition: null,
      };
    },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY
    }
  },
  
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
  },
  destroy() {
  window.removeEventListener('scroll', this.updateScroll)
}

}
</script>

<style lang="scss">

li {
 list-style-type: none;
}

a{
  text-decoration: none;
  color: white;
  box-shadow: 0px 0px 5px rgb(58, 58, 58);
  padding: 7px 15px;
  border-radius: 30px;
  background-color:rgba(0,0,0,.1);
}
a:hover{
    transition: 0.5s;
    background: rgb(175, 175, 175);
    opacity: 0.9;
}
a, p, span {
  font-family:  'Raleway', sans-serif;
}
p {
  color: #58666e;
}
body {
  margin: 0;
  padding: 0;
}
.app {
  width: 100%;
}
</style>
