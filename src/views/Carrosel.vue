<template>
    <div id="items-wropper">
        <div id="items">
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
            <div class="items"><img src="https://picsum.photos/200/300"/></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Carrosel',
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    height: 100vh;
}

body {
    display: grid;
    place-items: center;
}

#items-wropper {
    width: 100vw;
}

#items {
    display: flex;
    overflow-x: auto;
}

.item {
    flex: none;

    width: 30%;
    height: 400px;
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>