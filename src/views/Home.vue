<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  mounted() {
    const postWrap = document.querySelector(".home");

    const bar = document.createElement("div");

    bar.style.height = "4px";
    bar.style.width = "500px";
    bar.style.backgroundColor = "$6633cc";
    bar.style.position = "fixed";
    bar.style.top = "0";
    bar.style.left = "0";
    bar.style.zIndex = "9999";
    bar.style.transition = "0.2s";

    document.body.append(bar);

    document.addEventListener("scroll", () => {
      const textHeight = postWrap.offsetHeight;
      const pagePositionY =  window.pageYOffset;

      const updateBar = pagePositionY * 100 / textHeight;

      bar.style.width = updateBar + "%";

      console.log(bar.style.width);
    });
  },
}
</script>
