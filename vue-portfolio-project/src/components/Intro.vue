<template>
    <div id="intro">
        <h2>SASHA ROBINSON</h2>
        <h1>McMASTER STUDENT & PROGRAMMER</h1>
        <h2>VIEW PROJECTS OR LEARN ABOUT ME</h2>
    </div>
</template>

<script>
export default {
    name: 'Intro'
}
</script>

<style>
#intro {
    position: relative;
    top: 9em;
    left: 3em;
    width: 40%;
}

h1 {
    font-family: 'Tusker Grotesk';
    font-style: normal;
    font-weight: 4500 Medium;
    font-size: 5em;
    letter-spacing: 0.15em;
    color: white;
    text-shadow: 0px 4px 4px
        rgba(0,0,0,0.25);
    margin-block: 0 0;
}

h2 {
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

@font-face {
    font-family: Tusker Grotesk;
    font-weight: 4500 Medium;
    src: url("../assets/TuskerGrotesk-4500Medium.ttf");
}
</style>