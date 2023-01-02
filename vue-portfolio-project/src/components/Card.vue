<template>
    <div class="card">
        <h2 class="h2-text-styling-intro" id="year">
            {{year}}
        </h2>
        <h2 class="sub-title-2" id="project-title">
            {{project}} 
        </h2>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        year: String,
        project: String,
        
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
    border-radius: 0.3em;
    background-color: skyblue;
    height: 40em;
    width: 30em;
    padding: 2em;
    margin: 1.5em;
    box-shadow: 0 4px 8px 0
        rgba(0,0,0,0.25);
    

}
.card:hover {
    box-shadow: 0 8px 16px 0 
        rgba(0,0,0,0.25)
}
</style>