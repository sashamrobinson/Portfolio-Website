<template>
    <div class="card" id="card" :style="bgStyle">
        <!-- <style="background-image: url('@/assets/logo.png');" -->
        <h2 class="h2-text-styling-intro" id="year">
            {{year}}
        </h2>
        <h2 class="sub-title-2" id="project-title">
            {{projectTitle}}
        </h2>
        <!-- <a href="https://www.freepik.com/free-psd/phone-14-pro-mockup_31761199.htm#query=iphone&position=4&from_view=search&track=sph">Image by qalebstudio</a> on Freepik -->
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        imageUrl: String,
        year: String,
        projectTitle: String
    },
    computed: {  
        bgStyle() {
            return {'background-image' : `url(${this.imageUrl})`}
        }
    }
}
</script>

<style>
#year {
    color: #6D6868;

}
#project-title {
    color: black;
    text-shadow: none;
    font-size: 1.5em;
}
.card {
    transition: 0.3s;
    height: 40em;
    width: 30em;
    padding: 2em;
    margin: 1em;
    box-shadow: 0 4px 8px 0
        rgba(0,0,0,0.25);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    

}
.card:hover {
    box-shadow: 0 8px 16px 0 
        rgba(0,0,0,0.25);
}
</style>