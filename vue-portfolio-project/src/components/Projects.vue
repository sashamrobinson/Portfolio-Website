<template>
    <div>
        <div id="projects">
            <h2 class="sub-title">PERSONAL</h2>
            <h1>PROJECTS</h1>
        </div>
        <table id="table-styling">
            <tr>
                <td><Card year="2023 - Winter" project="Portfolio Project"/></td>
                <td><Card year="2021 - Fall" project="PlayBetter"/></td>
            </tr>
            <tr>
                <td><Card year="2020 - Summer" project="ListList"/></td>
                <td><Card year="2020 - Spring" project="Harvester"/></td>
            </tr>
            </table>
    </div>
</template>

<script>
import Card from './Card'
export default {
    name: 'Projects',
    components: {
        Card
    }
}
</script>

<style>
#table-styling {
    margin-left: auto;
    margin-right: auto;
}
#projects {
    position: relative;
    margin-top: 36em;
    left: 5em;    
}
</style>