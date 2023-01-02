<template>
    <div id="about">
        <h2 class="sub-title">ABOUT ME</h2>
        <h2 class="h2-text-styling-intro" id="para"> Hello, I am a first-year student at McMaster University who has spent
             the past couple years designing and creating personal projects using a variety of different languages
              and frameworks.</h2>
    </div>
</template>

<script>
export default {
    name: 'AboutMe'
}
</script>

<style>
#about {
    position: absolute;
    margin-top: 18em;
    right: 5em;
    width: 45%;
    text-align: right;
}
#para {
    letter-spacing: 0.15em;
    line-height: 1.5em;
}
.h2-text-styling-intro {
    font-family: 'Tahoma';
    font-style: normal;
    font-weight: 400;
    font-size: 1.2em;
    letter-spacing: 0.1em;
    margin-block: 0 0;
    color: white;
    text-shadow: 0px 4px 4px
        rgba(0,0,0,0.25); 
}
</style>