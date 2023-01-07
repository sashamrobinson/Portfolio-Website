<template>
    <div>
        <div id="projects">
            <h2 class="sub-title">PERSONAL</h2>
            <h1>PROJECTS</h1>
        </div>
        <table id="table-styling">
            <tr>
                <td><Card :year="projects[0].year" :projectTitle="projects[0].projectTitle" :imageUrl="projects[0].imageUrl"/></td>
                <td><Card :year="projects[1].year" :projectTitle="projects[1].projectTitle" :imageUrl="projects[1].imageUrl"/></td>
            </tr>
            <tr>
                <td><Card :year="projects[2].year" :projectTitle="projects[2].projectTitle" :imageUrl="projects[2].imageUrl"/></td>
                <td><Card :year="projects[3].year" :projectTitle="projects[3].projectTitle" :imageUrl="projects[3].imageUrl"/></td>
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
    },
    data() {
        return {
            // imageUrl: require("../assets/laptop_mockup.png")
            projects: [
                {id: 1, year: '2023 - Winter', projectTitle: 'Portfolio Project', imageUrl: require("../assets/Mockup.png")},
                {id: 2, year: '2020 - Summer', projectTitle: 'ListList', imageUrl: require("../assets/phone_14_pro_mockup_2.png")},
                {id: 3, year: '2021 - Fall', projectTitle: 'PlayBetter', imageUrl: require("../assets/laptop_mockup.png")},
                {id: 4, year: '2020 - Spring', projectTitle: 'Other Apps', imageUrl: require("../assets/laptop_mockup.png")}
            ]
        }
    },
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