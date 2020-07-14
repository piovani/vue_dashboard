<template>
  <div class="home">
    <Carrosel></Carrosel>
  </div>
</template>

<script>
import Carrosel from '@/views/Carrosel.vue'

export default {
  name: 'Home',
  components: {
    Carrosel
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
