<template>
    <div id="align">
        <h1 class="menuText">MENU</h1>
        <img src="../assets/menu_icon.png" alt="">
    </div>
</template>

<script>
export default {
    name: 'Menu',
    components: {
        
    }
}
</script>

<style>
#align {
    display: flex;
    margin: 1em;
}
.menuText {
    font-family: "Tahoma";
    font-style: normal;
    font-weight: 700;
    font-size: 1em;
    letter-spacing: 0.045em;
    color: white;
    margin-right: 1em;
    text-shadow: 0px 4px 4px
        rgba(0, 0, 0, 0.25)
}
</style>