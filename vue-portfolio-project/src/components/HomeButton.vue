<template>
    <div>
        <router-link to="/" id="homeButton">HOME</router-link>
    </div>
</template>

<script>
export default {
    name: 'HomeButton'
}
</script>

<style>
#homeButton {
    /* NEEDS TO BE CHANGED */
    font-family: "Tahoma";
    font-style: normal;
    font-weight: 700;
    font-size: 2em;
    letter-spacing: 0.045em;
    color: white;
    text-decoration: none;
    text-shadow: 0px 4px 4px
        rgba(0, 0, 0, 0.25)
}
</style>